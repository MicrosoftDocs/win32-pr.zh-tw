---
title: Residential-Person 類別
description: 用來定義代表居住環境中人員的專案。
ms.assetid: 7d11e4a7-2824-4eb2-8c87-48113e65c936
ms.tgt_platform: multiple
keywords:
- Residential-Person 類別 AD 架構
- residentialPerson 類別 AD 架構
topic_type:
- apiref
api_name:
- Residential-Person
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3684c2b8b28a4868f349fa5a74a4856cb9d7f45fc94d83c33211abb4529631cf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118959667"
---
# <a name="residential-person-class"></a>Residential-Person 類別

用來定義代表居住環境中人員的專案。



| 進入 | 值 |
|-------------------|--------------------------------------|
| CN                | Residential-Person                   |
| Ldap-顯示名稱 | residentialPerson                    |
| 更新許可權  | \-                                   |
| 更新頻率  | \-                                   |
| 架構識別碼-Guid    | a8df74d6-c5ea-11d1-bbcb-0080c76670c0 |



## <a name="implementations"></a>實作

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server

-   [屬性](#windows-2000-server-attributes)



| 進入 | 值 |
|-----------------------------|----------------------------------------------------------------------------------------------|
| System-Only                 | 否                                                                                        |
| Object-Category             | 1                                                                                            |
| 預設-物件-類別     | \-                                                                                           |
| Governs-Id                  | 2.5.6.10                                                                                     |
| 預設值-隱藏-值        | 1                                                                                            |
| Rdn-Att-Id                  | [**一般名稱**](a-cn.md)<br/>                                                       |
| 的子類別                 | [**人**](c-person.md)<br/>                                                        |
| 可能的 Superiors          | [**容器**](c-container.md)                                                             |
| 輔助類別           | \-                                                                                           |
| NT-Security-描述元      | O:BAG：不正確： S：                                                                                 |
| 預設安全描述項 | D:(A;;RPWPCRCCDCLCLORCWOWDSDDTSW;;;DA)(A;;RPWPCRCCDCLCLORCWOWDSDDTSW;;;SY)(A;;RPLCLORC;;;AU) |
| System-Flags                | 0x00000010                                                                                   |



## <a name="windows-2000-server-attributes"></a>Windows 2000 伺服器屬性

此類別包含 Windows 2000 伺服器的下列屬性：



| 屬性                                                                 | 強制性 | 衍生自                                                          |
|---------------------------------------------------------------------------|-----------|-----------------------------------------------------------------------|
| [**系統管理員-描述**](a-admindescription.md)                           | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**系統管理員-顯示名稱**](a-admindisplayname.md)                          | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**允許-屬性**](a-allowedattributes.md)                         | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**允許-屬性-有效**](a-allowedattributeseffective.md)      | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**允許-子類別**](a-allowedchildclasses.md)                    | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**允許-子類別-有效**](a-allowedchildclasseseffective.md) | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**橋頭-伺服器-清單-BL**](a-bridgeheadserverlistbl.md)             | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**商務-類別**](a-businesscategory.md)                           | 否     | **居住人**                                                |
| [**標準名稱**](a-canonicalname.md)                                 | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**一般名稱**](a-cn.md)                                               | 是      | [**人**](c-person.md)<br/> [**返回頁首**](c-top.md)<br/> |
| [**建立時間戳記**](a-createtimestamp.md)                            | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**描述**](a-description.md)                                      | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**目的地-指標**](a-destinationindicator.md)                   | 否     | **居住人**                                                |
| [**顯示名稱**](a-displayname.md)                                     | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**顯示-名稱-可列印**](a-displaynameprintable.md)                  | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**DSA-簽章**](a-dsasignature.md)                                   | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**DS-核心-傳播-資料**](a-dscorepropagationdata.md)               | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**副檔名-名稱**](a-extensionname.md)                                 | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**傳真-電話號碼**](a-facsimiletelephonenumber.md)          | 否     | **居住人**                                                |
| [**標誌**](a-flags.md)                                                  | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**從-進入**](a-fromentry.md)                                         | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**Frs-電腦-參考-BL**](a-frscomputerreferencebl.md)             | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**FRS-成員參考-BL**](a-frsmemberreferencebl.md)                 | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**FSMO 角色-擁有者**](a-fsmoroleowner.md)                                | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**實例類型**](a-instancetype.md)                                   | 是      | [**返回頁首**](c-top.md)<br/>                                       |
| [**國際 ISDN 號碼**](a-internationalisdnnumber.md)            | 否     | **居住人**                                                |
| [**為關鍵-系統物件**](a-iscriticalsystemobject.md)             | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**已刪除**](a-isdeleted.md)                                         | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**是-DL 的成員**](a-memberof.md)                                     | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**是-許可權-持有者**](a-isprivilegeholder.md)                        | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**最後一個已知-父系**](a-lastknownparent.md)                            | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**位置名稱**](a-l.md)                                              | 否     | **居住人**                                                |
| [**Managed 物件**](a-managedobjects.md)                               | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**主要**](a-masteredby.md)                                       | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**修改時間戳記**](a-modifytimestamp.md)                            | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**MS DS-一致性-子計數**](a-ms-ds-consistencychildcount.md)    | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                 | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**netboot-SCP-BL**](a-netbootscpbl.md)                                  | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**非安全性成員-BL**](a-nonsecuritymemberbl.md)                   | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**NT-Security-描述元**](a-ntsecuritydescriptor.md)                  | 是      | [**返回頁首**](c-top.md)<br/>                                       |
| [**Obj-Dist 名稱**](a-distinguishedname.md)                              | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**物件-類別**](a-objectcategory.md)                               | 是      | [**返回頁首**](c-top.md)<br/>                                       |
| [**物件類別**](a-objectclass.md)                                     | 是      | [**返回頁首**](c-top.md)<br/>                                       |
| [**物件-Guid**](a-objectguid.md)                                       | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**物件版本**](a-objectversion.md)                                 | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**組織單位-名稱**](a-ou.md)                                  | 否     | **居住人**                                                |
| [**其他知名物件**](a-otherwellknownobjects.md)               | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**部分屬性-刪除-清單**](a-partialattributedeletionlist.md) | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**部分屬性集**](a-partialattributeset.md)                    | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**實體傳遞-Office-名稱**](a-physicaldeliveryofficename.md)     | 否     | **居住人**                                                |
| [**可能-Inferiors**](a-possibleinferiors.md)                         | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**郵件標籤**](a-postaladdress.md)                                 | 否     | **居住人**                                                |
| [**郵遞區號**](a-postalcode.md)                                       | 否     | **居住人**                                                |
| [**後續 Office-Box**](a-postofficebox.md)                                | 否     | **居住人**                                                |
| [**慣用傳遞方法**](a-preferreddeliverymethod.md)            | 否     | **居住人**                                                |
| [**Proxy-物件名稱**](a-proxiedobjectname.md)                        | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**Proxy 位址**](a-proxyaddresses.md)                               | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**查詢-原則-BL**](a-querypolicybl.md)                                | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**RDN**](a-name.md)                                                     | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**登入位址**](a-registeredaddress.md)                         | 否     | **居住人**                                                |
| [**複寫-屬性中繼資料**](a-replpropertymetadata.md)                 | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**複寫-UpToDate-向量**](a-repluptodatevector.md)                      | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**報表**](a-directreports.md)                                        | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**代表-來源**](a-repsfrom.md)                                           | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**代表**](a-repsto.md)                                               | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**修訂**](a-revision.md)                                            | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**SD-Rights-有效**](a-sdrightseffective.md)                        | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**請參閱-也**](a-seealso.md)                                             | 否     | [**人**](c-person.md)<br/>                                 |
| [**伺服器參考-BL**](a-serverreferencebl.md)                        | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**顯示-內建-僅限視圖**](a-showinadvancedviewonly.md)            | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**網站-物件-BL**](a-siteobjectbl.md)                                  | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**州/省名稱**](a-st.md)                                    | 否     | **居住人**                                                |
| [**街道位址**](a-street.md)                                        | 否     | **居住人**                                                |
| [**子 Refs**](a-subrefs.md)                                             | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                          | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**姓**](a-sn.md)                                                   | 否     | [**人**](c-person.md)<br/>                                 |
| [**系統旗標**](a-systemflags.md)                                     | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**電話號碼**](a-telephonenumber.md)                             | 否     | [**人**](c-person.md)<br/>                                 |
| [**Teletex-終端機-識別碼**](a-teletexterminalidentifier.md)        | 否     | **居住人**                                                |
| [**電傳號碼**](a-telexnumber.md)                                     | 否     | **居住人**                                                |
| [**標題**](a-title.md)                                                  | 否     | **居住人**                                                |
| [**使用者-密碼**](a-userpassword.md)                                   | 否     | [**人**](c-person.md)<br/>                                 |
| [**USN-已變更**](a-usnchanged.md)                                       | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**USN-已建立**](a-usncreated.md)                                       | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**USN-已移除-最後-Obj**](a-usndsalastobjremoved.md)                | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**USN-站間**](a-usnintersite.md)                                   | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**USN-最後-Obj-Rem**](a-usnlastobjrem.md)                               | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**USN-來源**](a-usnsource.md)                                         | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**Wbem-路徑**](a-wbempath.md)                                           | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**知名物件**](a-wellknownobjects.md)                          | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**變更時**](a-whenchanged.md)                                     | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**建立時間**](a-whencreated.md)                                     | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**WWW-首頁**](a-wwwhomepage.md)                                    | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**WWW-頁面-其他**](a-url.md)                                           | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**X121-位址**](a-x121address.md)                                     | 否     | **居住人**                                                |



## <a name="windows-server-2003"></a>Windows Server 2003

-   [屬性](#windows-server-2003-attributes)



| 進入 | 值 |
|-----------------------------|----------------------------------------------------------------------------------------------|
| System-Only                 | 否                                                                                        |
| Object-Category             | 1                                                                                            |
| 預設-物件-類別     | \-                                                                                           |
| Governs-Id                  | 2.5.6.10                                                                                     |
| 預設值-隱藏-值        | 1                                                                                            |
| Rdn-Att-Id                  | [**一般名稱**](a-cn.md)<br/>                                                       |
| 的子類別                 | [**人**](c-person.md)<br/>                                                        |
| 可能的 Superiors          | [**容器**](c-container.md)[**位置**](c-locality.md)                               |
| 輔助類別           | \-                                                                                           |
| NT-Security-描述元      | O:BAG：不正確： S：                                                                                 |
| 預設安全描述項 | D:(A;;RPWPCRCCDCLCLORCWOWDSDDTSW;;;DA)(A;;RPWPCRCCDCLCLORCWOWDSDDTSW;;;SY)(A;;RPLCLORC;;;AU) |
| System-Flags                | 0x00000010                                                                                   |



## <a name="windows-server-2003-attributes"></a>Windows伺服器2003屬性

此類別包含 Windows Server 2003 的下列屬性：



| 屬性                                                                   | 強制性 | 衍生自                                                          |
|-----------------------------------------------------------------------------|-----------|-----------------------------------------------------------------------|
| [**系統管理員-描述**](a-admindescription.md)                             | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**系統管理員-顯示名稱**](a-admindisplayname.md)                            | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**允許-屬性**](a-allowedattributes.md)                           | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**允許-屬性-有效**](a-allowedattributeseffective.md)        | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**允許-子類別**](a-allowedchildclasses.md)                      | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**允許-子類別-有效**](a-allowedchildclasseseffective.md)   | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**attributeCertificateAttribute**](a-attributecertificateattribute.md)    | 否     | [**人**](c-person.md)<br/>                                 |
| [**橋頭-伺服器-清單-BL**](a-bridgeheadserverlistbl.md)               | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**商務-類別**](a-businesscategory.md)                             | 否     | **居住人**                                                |
| [**標準名稱**](a-canonicalname.md)                                   | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**一般名稱**](a-cn.md)                                                 | 是      | [**人**](c-person.md)<br/> [**返回頁首**](c-top.md)<br/> |
| [**建立時間戳記**](a-createtimestamp.md)                              | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**描述**](a-description.md)                                        | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**目的地-指標**](a-destinationindicator.md)                     | 否     | **居住人**                                                |
| [**顯示名稱**](a-displayname.md)                                       | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**顯示-名稱-可列印**](a-displaynameprintable.md)                    | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**DSA-簽章**](a-dsasignature.md)                                     | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**DS-核心-傳播-資料**](a-dscorepropagationdata.md)                 | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**副檔名-名稱**](a-extensionname.md)                                   | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**傳真-電話號碼**](a-facsimiletelephonenumber.md)            | 否     | **居住人**                                                |
| [**標誌**](a-flags.md)                                                    | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**從-進入**](a-fromentry.md)                                           | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**Frs-電腦-參考-BL**](a-frscomputerreferencebl.md)               | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**FRS-成員參考-BL**](a-frsmemberreferencebl.md)                   | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**FSMO 角色-擁有者**](a-fsmoroleowner.md)                                  | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**實例類型**](a-instancetype.md)                                     | 是      | [**返回頁首**](c-top.md)<br/>                                       |
| [**國際 ISDN 號碼**](a-internationalisdnnumber.md)              | 否     | **居住人**                                                |
| [**為關鍵-系統物件**](a-iscriticalsystemobject.md)               | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**已刪除**](a-isdeleted.md)                                           | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**是-DL 的成員**](a-memberof.md)                                       | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**是-許可權-持有者**](a-isprivilegeholder.md)                          | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**最後一個已知-父系**](a-lastknownparent.md)                              | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**位置名稱**](a-l.md)                                                | 否     | **居住人**                                                |
| [**Managed 物件**](a-managedobjects.md)                                 | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**主要**](a-masteredby.md)                                         | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**修改時間戳記**](a-modifytimestamp.md)                              | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**PartitionSetLink**](a-mscom-partitionsetlink.md)                 | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**UserLink**](a-mscom-userlink.md)                                 | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**ms-DS-Immed-從屬**](a-msds-approx-immed-subordinates.md) | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**MS DS-一致性-子計數**](a-ms-ds-consistencychildcount.md)      | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                   | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**ms DS-主要-依據**](a-msds-masteredby.md)                              | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**ms DS-成員--Az-Role-BL**](a-msds-membersforazrolebl.md)           | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**ms DS-NC-複寫-資料指標**](a-msds-ncreplcursors.md)                       | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**ms-DS-NC-複寫-輸入-相鄰**](a-msds-ncreplinboundneighbors.md)    | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**ms DS-NC-複寫-輸出-相鄰**](a-msds-ncreploutboundneighbors.md)  | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**ms DS-非成員-BL**](a-msds-nonmembersbl.md)                         | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**BL-------物件參考**](a-msds-objectreferencebl.md)               | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**BL-------------------**](a-msds-operationsforazrolebl.md)     | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**BL-------------工作-**](a-msds-operationsforaztaskbl.md)     | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**ms-DS-複寫-屬性中繼資料**](a-msds-replattributemetadata.md)      | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**ms-DS-複製-值中繼資料**](a-msds-replvaluemetadata.md)              | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**ms-chap---------BL**](a-msds-tasksforazrolebl.md)               | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**ms DS-工作--Az-Task-BL**](a-msds-tasksforaztaskbl.md)               | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**Ms-exch-assistant-name-擁有者-BL**](a-ownerbl.md)                                       | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**netboot-SCP-BL**](a-netbootscpbl.md)                                    | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**非安全性成員-BL**](a-nonsecuritymemberbl.md)                     | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**NT-Security-描述元**](a-ntsecuritydescriptor.md)                    | 是      | [**返回頁首**](c-top.md)<br/>                                       |
| [**Obj-Dist 名稱**](a-distinguishedname.md)                                | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**物件-類別**](a-objectcategory.md)                                 | 是      | [**返回頁首**](c-top.md)<br/>                                       |
| [**物件類別**](a-objectclass.md)                                       | 是      | [**返回頁首**](c-top.md)<br/>                                       |
| [**物件-Guid**](a-objectguid.md)                                         | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**物件版本**](a-objectversion.md)                                   | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**組織單位-名稱**](a-ou.md)                                    | 否     | **居住人**                                                |
| [**其他知名物件**](a-otherwellknownobjects.md)                 | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**部分屬性-刪除-清單**](a-partialattributedeletionlist.md)   | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**部分屬性集**](a-partialattributeset.md)                      | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**實體傳遞-Office-名稱**](a-physicaldeliveryofficename.md)       | 否     | **居住人**                                                |
| [**可能-Inferiors**](a-possibleinferiors.md)                           | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**郵件標籤**](a-postaladdress.md)                                   | 否     | **居住人**                                                |
| [**郵遞區號**](a-postalcode.md)                                         | 否     | **居住人**                                                |
| [**後續 Office-Box**](a-postofficebox.md)                                  | 否     | **居住人**                                                |
| [**慣用傳遞方法**](a-preferreddeliverymethod.md)              | 否     | **居住人**                                                |
| [**Proxy-物件名稱**](a-proxiedobjectname.md)                          | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**Proxy 位址**](a-proxyaddresses.md)                                 | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**查詢-原則-BL**](a-querypolicybl.md)                                  | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**RDN**](a-name.md)                                                       | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**登入位址**](a-registeredaddress.md)                           | 否     | **居住人**                                                |
| [**複寫-屬性中繼資料**](a-replpropertymetadata.md)                   | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**複寫-UpToDate-向量**](a-repluptodatevector.md)                        | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**報表**](a-directreports.md)                                          | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**代表-來源**](a-repsfrom.md)                                             | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**代表**](a-repsto.md)                                                 | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**修訂**](a-revision.md)                                              | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**SD-Rights-有效**](a-sdrightseffective.md)                          | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**請參閱-也**](a-seealso.md)                                               | 否     | [**人**](c-person.md)<br/>                                 |
| [**序號**](a-serialnumber.md)                                     | 否     | [**人**](c-person.md)<br/>                                 |
| [**伺服器參考-BL**](a-serverreferencebl.md)                          | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**顯示-內建-僅限視圖**](a-showinadvancedviewonly.md)              | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**網站-物件-BL**](a-siteobjectbl.md)                                    | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**州/省名稱**](a-st.md)                                      | 否     | **居住人**                                                |
| [**街道位址**](a-street.md)                                          | 否     | **居住人**                                                |
| [**結構物件類別**](a-structuralobjectclass.md)                  | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**子 Refs**](a-subrefs.md)                                               | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                            | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**姓**](a-sn.md)                                                     | 否     | [**人**](c-person.md)<br/>                                 |
| [**系統旗標**](a-systemflags.md)                                       | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**電話號碼**](a-telephonenumber.md)                               | 否     | [**人**](c-person.md)<br/>                                 |
| [**Teletex-終端機-識別碼**](a-teletexterminalidentifier.md)          | 否     | **居住人**                                                |
| [**電傳號碼**](a-telexnumber.md)                                       | 否     | **居住人**                                                |
| [**標題**](a-title.md)                                                    | 否     | **居住人**                                                |
| [**使用者-密碼**](a-userpassword.md)                                     | 否     | [**人**](c-person.md)<br/>                                 |
| [**USN-已變更**](a-usnchanged.md)                                         | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**USN-已建立**](a-usncreated.md)                                         | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**USN-已移除-最後-Obj**](a-usndsalastobjremoved.md)                  | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**USN-站間**](a-usnintersite.md)                                     | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**USN-最後-Obj-Rem**](a-usnlastobjrem.md)                                 | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**USN-來源**](a-usnsource.md)                                           | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**Wbem-路徑**](a-wbempath.md)                                             | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**知名物件**](a-wellknownobjects.md)                            | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**變更時**](a-whenchanged.md)                                       | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**建立時間**](a-whencreated.md)                                       | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**WWW-首頁**](a-wwwhomepage.md)                                      | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**WWW-頁面-其他**](a-url.md)                                             | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**X121-位址**](a-x121address.md)                                       | 否     | **居住人**                                                |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2

-   [屬性](#windows-server-2003-r2-attributes)



| 進入 | 值 |
|-----------------------------|----------------------------------------------------------------------------------------------|
| System-Only                 | 否                                                                                        |
| Object-Category             | 1                                                                                            |
| 預設-物件-類別     | \-                                                                                           |
| Governs-Id                  | 2.5.6.10                                                                                     |
| 預設值-隱藏-值        | 1                                                                                            |
| Rdn-Att-Id                  | [**一般名稱**](a-cn.md)<br/>                                                       |
| 的子類別                 | [**人**](c-person.md)<br/>                                                        |
| 可能的 Superiors          | [**容器**](c-container.md)[**位置**](c-locality.md)                               |
| 輔助類別           | \-                                                                                           |
| NT-Security-描述元      | O:BAG：不正確： S：                                                                                 |
| 預設安全描述項 | D:(A;;RPWPCRCCDCLCLORCWOWDSDDTSW;;;DA)(A;;RPWPCRCCDCLCLORCWOWDSDDTSW;;;SY)(A;;RPLCLORC;;;AU) |
| System-Flags                | 0x00000010                                                                                   |



## <a name="windows-server-2003-r2-attributes"></a>WindowsServer 2003 R2 屬性

此類別包含 Windows Server 2003 R2 的下列屬性：



| 屬性                                                                   | 強制性 | 衍生自                                                          |
|-----------------------------------------------------------------------------|-----------|-----------------------------------------------------------------------|
| [**系統管理員-描述**](a-admindescription.md)                             | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**系統管理員-顯示名稱**](a-admindisplayname.md)                            | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**允許-屬性**](a-allowedattributes.md)                           | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**允許-屬性-有效**](a-allowedattributeseffective.md)        | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**允許-子類別**](a-allowedchildclasses.md)                      | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**允許-子類別-有效**](a-allowedchildclasseseffective.md)   | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**attributeCertificateAttribute**](a-attributecertificateattribute.md)    | 否     | [**人**](c-person.md)<br/>                                 |
| [**橋頭-伺服器-清單-BL**](a-bridgeheadserverlistbl.md)               | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**商務-類別**](a-businesscategory.md)                             | 否     | **居住人**                                                |
| [**標準名稱**](a-canonicalname.md)                                   | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**一般名稱**](a-cn.md)                                                 | 是      | [**人**](c-person.md)<br/> [**返回頁首**](c-top.md)<br/> |
| [**建立時間戳記**](a-createtimestamp.md)                              | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**描述**](a-description.md)                                        | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**目的地-指標**](a-destinationindicator.md)                     | 否     | **居住人**                                                |
| [**顯示名稱**](a-displayname.md)                                       | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**顯示-名稱-可列印**](a-displaynameprintable.md)                    | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**DSA-簽章**](a-dsasignature.md)                                     | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**DS-核心-傳播-資料**](a-dscorepropagationdata.md)                 | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**副檔名-名稱**](a-extensionname.md)                                   | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**傳真-電話號碼**](a-facsimiletelephonenumber.md)            | 否     | **居住人**                                                |
| [**標誌**](a-flags.md)                                                    | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**從-進入**](a-fromentry.md)                                           | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**Frs-電腦-參考-BL**](a-frscomputerreferencebl.md)               | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**FRS-成員參考-BL**](a-frsmemberreferencebl.md)                   | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**FSMO 角色-擁有者**](a-fsmoroleowner.md)                                  | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**實例類型**](a-instancetype.md)                                     | 是      | [**返回頁首**](c-top.md)<br/>                                       |
| [**國際 ISDN 號碼**](a-internationalisdnnumber.md)              | 否     | **居住人**                                                |
| [**為關鍵-系統物件**](a-iscriticalsystemobject.md)               | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**已刪除**](a-isdeleted.md)                                           | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**是-DL 的成員**](a-memberof.md)                                       | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**是-許可權-持有者**](a-isprivilegeholder.md)                          | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**最後一個已知-父系**](a-lastknownparent.md)                              | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**位置名稱**](a-l.md)                                                | 否     | **居住人**                                                |
| [**Managed 物件**](a-managedobjects.md)                                 | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**主要**](a-masteredby.md)                                         | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**修改時間戳記**](a-modifytimestamp.md)                              | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**PartitionSetLink**](a-mscom-partitionsetlink.md)                 | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**UserLink**](a-mscom-userlink.md)                                 | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**ms-DFSR-ComputerReferenceBL**](a-msdfsr-computerreferencebl.md)         | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**ms-DFSR-MemberReferenceBL**](a-msdfsr-memberreferencebl.md)             | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**ms-DS-Immed-從屬**](a-msds-approx-immed-subordinates.md) | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**MS DS-一致性-子計數**](a-ms-ds-consistencychildcount.md)      | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                   | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**ms DS-主要-依據**](a-msds-masteredby.md)                              | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**ms DS-成員--Az-Role-BL**](a-msds-membersforazrolebl.md)           | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**ms DS-NC-複寫-資料指標**](a-msds-ncreplcursors.md)                       | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**ms-DS-NC-複寫-輸入-相鄰**](a-msds-ncreplinboundneighbors.md)    | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**ms DS-NC-複寫-輸出-相鄰**](a-msds-ncreploutboundneighbors.md)  | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**ms DS-非成員-BL**](a-msds-nonmembersbl.md)                         | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**BL-------物件參考**](a-msds-objectreferencebl.md)               | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**BL-------------------**](a-msds-operationsforazrolebl.md)     | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**BL-------------工作-**](a-msds-operationsforaztaskbl.md)     | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**ms-DS-複寫-屬性中繼資料**](a-msds-replattributemetadata.md)      | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**ms-DS-複製-值中繼資料**](a-msds-replvaluemetadata.md)              | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**ms-chap---------BL**](a-msds-tasksforazrolebl.md)               | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**ms DS-工作--Az-Task-BL**](a-msds-tasksforaztaskbl.md)               | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**Ms-exch-assistant-name-擁有者-BL**](a-ownerbl.md)                                       | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**msSFU-30-Posix-成員**](a-mssfu30posixmemberof.md)                  | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**netboot-SCP-BL**](a-netbootscpbl.md)                                    | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**非安全性成員-BL**](a-nonsecuritymemberbl.md)                     | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**NT-Security-描述元**](a-ntsecuritydescriptor.md)                    | 是      | [**返回頁首**](c-top.md)<br/>                                       |
| [**Obj-Dist 名稱**](a-distinguishedname.md)                                | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**物件-類別**](a-objectcategory.md)                                 | 是      | [**返回頁首**](c-top.md)<br/>                                       |
| [**物件類別**](a-objectclass.md)                                       | 是      | [**返回頁首**](c-top.md)<br/>                                       |
| [**物件-Guid**](a-objectguid.md)                                         | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**物件版本**](a-objectversion.md)                                   | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**組織單位-名稱**](a-ou.md)                                    | 否     | **居住人**                                                |
| [**其他知名物件**](a-otherwellknownobjects.md)                 | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**部分屬性-刪除-清單**](a-partialattributedeletionlist.md)   | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**部分屬性集**](a-partialattributeset.md)                      | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**實體傳遞-Office-名稱**](a-physicaldeliveryofficename.md)       | 否     | **居住人**                                                |
| [**可能-Inferiors**](a-possibleinferiors.md)                           | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**郵件標籤**](a-postaladdress.md)                                   | 否     | **居住人**                                                |
| [**郵遞區號**](a-postalcode.md)                                         | 否     | **居住人**                                                |
| [**後續 Office-Box**](a-postofficebox.md)                                  | 否     | **居住人**                                                |
| [**慣用傳遞方法**](a-preferreddeliverymethod.md)              | 否     | **居住人**                                                |
| [**Proxy-物件名稱**](a-proxiedobjectname.md)                          | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**Proxy 位址**](a-proxyaddresses.md)                                 | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**查詢-原則-BL**](a-querypolicybl.md)                                  | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**RDN**](a-name.md)                                                       | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**登入位址**](a-registeredaddress.md)                           | 否     | **居住人**                                                |
| [**複寫-屬性中繼資料**](a-replpropertymetadata.md)                   | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**複寫-UpToDate-向量**](a-repluptodatevector.md)                        | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**報表**](a-directreports.md)                                          | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**代表-來源**](a-repsfrom.md)                                             | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**代表**](a-repsto.md)                                                 | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**修訂**](a-revision.md)                                              | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**SD-Rights-有效**](a-sdrightseffective.md)                          | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**請參閱-也**](a-seealso.md)                                               | 否     | [**人**](c-person.md)<br/>                                 |
| [**序號**](a-serialnumber.md)                                     | 否     | [**人**](c-person.md)<br/>                                 |
| [**伺服器參考-BL**](a-serverreferencebl.md)                          | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**顯示-內建-僅限視圖**](a-showinadvancedviewonly.md)              | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**網站-物件-BL**](a-siteobjectbl.md)                                    | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**州/省名稱**](a-st.md)                                      | 否     | **居住人**                                                |
| [**街道位址**](a-street.md)                                          | 否     | **居住人**                                                |
| [**結構物件類別**](a-structuralobjectclass.md)                  | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**子 Refs**](a-subrefs.md)                                               | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                            | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**姓**](a-sn.md)                                                     | 否     | [**人**](c-person.md)<br/>                                 |
| [**系統旗標**](a-systemflags.md)                                       | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**電話號碼**](a-telephonenumber.md)                               | 否     | [**人**](c-person.md)<br/>                                 |
| [**Teletex-終端機-識別碼**](a-teletexterminalidentifier.md)          | 否     | **居住人**                                                |
| [**電傳號碼**](a-telexnumber.md)                                       | 否     | **居住人**                                                |
| [**標題**](a-title.md)                                                    | 否     | **居住人**                                                |
| [**使用者-密碼**](a-userpassword.md)                                     | 否     | [**人**](c-person.md)<br/>                                 |
| [**USN-已變更**](a-usnchanged.md)                                         | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**USN-已建立**](a-usncreated.md)                                         | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**USN-已移除-最後-Obj**](a-usndsalastobjremoved.md)                  | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**USN-站間**](a-usnintersite.md)                                     | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**USN-最後-Obj-Rem**](a-usnlastobjrem.md)                                 | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**USN-來源**](a-usnsource.md)                                           | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**Wbem-路徑**](a-wbempath.md)                                             | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**知名物件**](a-wellknownobjects.md)                            | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**變更時**](a-whenchanged.md)                                       | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**建立時間**](a-whencreated.md)                                       | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**WWW-首頁**](a-wwwhomepage.md)                                      | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**WWW-頁面-其他**](a-url.md)                                             | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**X121-位址**](a-x121address.md)                                       | 否     | **居住人**                                                |



## <a name="windows-server-2008"></a>Windows Server 2008

-   [屬性](#windows-server-2008-attributes)



| 進入 | 值 |
|-----------------------------|----------------------------------------------------------------------------------------------|
| System-Only                 | 否                                                                                        |
| Object-Category             | 1                                                                                            |
| 預設-物件-類別     | \-                                                                                           |
| Governs-Id                  | 2.5.6.10                                                                                     |
| 預設值-隱藏-值        | 1                                                                                            |
| Rdn-Att-Id                  | [**一般名稱**](a-cn.md)<br/>                                                       |
| 的子類別                 | [**人**](c-person.md)<br/>                                                        |
| 可能的 Superiors          | [**容器**](c-container.md)[**位置**](c-locality.md)                               |
| 輔助類別           | \-                                                                                           |
| NT-Security-描述元      | O:BAG：不正確： S：                                                                                 |
| 預設安全描述項 | D:(A;;RPWPCRCCDCLCLORCWOWDSDDTSW;;;DA)(A;;RPWPCRCCDCLCLORCWOWDSDDTSW;;;SY)(A;;RPLCLORC;;;AU) |
| System-Flags                | 0x00000010                                                                                   |



## <a name="windows-server-2008-attributes"></a>Windows伺服器2008屬性

此類別包含 Windows Server 2008 的下列屬性：



| 屬性                                                                      | 強制性 | 衍生自                                                          |
|--------------------------------------------------------------------------------|-----------|-----------------------------------------------------------------------|
| [**系統管理員-描述**](a-admindescription.md)                                | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**系統管理員-顯示名稱**](a-admindisplayname.md)                               | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**允許-屬性**](a-allowedattributes.md)                              | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**允許-屬性-有效**](a-allowedattributeseffective.md)           | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**允許-子類別**](a-allowedchildclasses.md)                         | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**允許-子類別-有效**](a-allowedchildclasseseffective.md)      | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**attributeCertificateAttribute**](a-attributecertificateattribute.md)       | 否     | [**人**](c-person.md)<br/>                                 |
| [**橋頭-伺服器-清單-BL**](a-bridgeheadserverlistbl.md)                  | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**商務-類別**](a-businesscategory.md)                                | 否     | **居住人**                                                |
| [**標準名稱**](a-canonicalname.md)                                      | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**一般名稱**](a-cn.md)                                                    | 是      | [**人**](c-person.md)<br/> [**返回頁首**](c-top.md)<br/> |
| [**建立時間戳記**](a-createtimestamp.md)                                 | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**描述**](a-description.md)                                           | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**目的地-指標**](a-destinationindicator.md)                        | 否     | **居住人**                                                |
| [**顯示名稱**](a-displayname.md)                                          | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**顯示-名稱-可列印**](a-displaynameprintable.md)                       | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**DSA-簽章**](a-dsasignature.md)                                        | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**DS-核心-傳播-資料**](a-dscorepropagationdata.md)                    | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**副檔名-名稱**](a-extensionname.md)                                      | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**傳真-電話號碼**](a-facsimiletelephonenumber.md)               | 否     | **居住人**                                                |
| [**標誌**](a-flags.md)                                                       | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**從-進入**](a-fromentry.md)                                              | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**Frs-電腦-參考-BL**](a-frscomputerreferencebl.md)                  | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**FRS-成員參考-BL**](a-frsmemberreferencebl.md)                      | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**FSMO 角色-擁有者**](a-fsmoroleowner.md)                                     | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**實例類型**](a-instancetype.md)                                        | 是      | [**返回頁首**](c-top.md)<br/>                                       |
| [**國際 ISDN 號碼**](a-internationalisdnnumber.md)                 | 否     | **居住人**                                                |
| [**為關鍵-系統物件**](a-iscriticalsystemobject.md)                  | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**已刪除**](a-isdeleted.md)                                              | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**是-DL 的成員**](a-memberof.md)                                          | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**是-許可權-持有者**](a-isprivilegeholder.md)                             | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**最後一個已知-父系**](a-lastknownparent.md)                                 | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**位置名稱**](a-l.md)                                                   | 否     | **居住人**                                                |
| [**Managed 物件**](a-managedobjects.md)                                    | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**主要**](a-masteredby.md)                                            | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**修改時間戳記**](a-modifytimestamp.md)                                 | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**PartitionSetLink**](a-mscom-partitionsetlink.md)                    | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**UserLink**](a-mscom-userlink.md)                                    | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**ms-DFSR-ComputerReferenceBL**](a-msdfsr-computerreferencebl.md)            | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**ms-DFSR-MemberReferenceBL**](a-msdfsr-memberreferencebl.md)                | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**ms-DS-Immed-從屬**](a-msds-approx-immed-subordinates.md)    | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**ms-DS-AuthenticatedTo-Accountlist**](a-msds-authenticatedtoaccountlist.md) | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**MS DS-一致性-子計數**](a-ms-ds-consistencychildcount.md)         | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                      | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**ms-DS-Is-Domain-For**](a-msds-isdomainfor.md)                              | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**ms-DS-Is-Full-Replica-For**](a-msds-isfullreplicafor.md)                   | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**ms-chap-為部分複本**](a-msds-ispartialreplicafor.md)             | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**ms-DS-KrbTgt-連結-BL**](a-msds-krbtgtlinkbl.md)                            | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**ms DS-主要-依據**](a-msds-masteredby.md)                                 | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**ms DS-成員--Az-Role-BL**](a-msds-membersforazrolebl.md)              | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**ms DS-NC-複寫-資料指標**](a-msds-ncreplcursors.md)                          | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**ms-DS-NC-複寫-輸入-相鄰**](a-msds-ncreplinboundneighbors.md)       | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**ms DS-NC-複寫-輸出-相鄰**](a-msds-ncreploutboundneighbors.md)     | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**ms DS-NC-RO-複本-位置-BL**](a-msds-nc-ro-replica-locations-bl.md)  | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**ms-DS-NC 類型**](a-msds-nctype.md)                                         | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**ms DS-非成員-BL**](a-msds-nonmembersbl.md)                            | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**BL-------物件參考**](a-msds-objectreferencebl.md)                  | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**BL-------------------**](a-msds-operationsforazrolebl.md)        | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**BL-------------工作-**](a-msds-operationsforaztaskbl.md)        | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**ms-DS-主體-名稱**](a-msds-principalname.md)                           | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**PSO-已套用**](a-msds-psoapplied.md)                                 | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**ms-DS-複寫-屬性中繼資料**](a-msds-replattributemetadata.md)         | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**ms-DS-複製-值中繼資料**](a-msds-replvaluemetadata.md)                 | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**ms-DS-顯示的 Dsa**](a-msds-revealeddsas.md)                             | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**ms-DS-Revealed-List-BL**](a-msds-revealedlistbl.md)                        | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**ms-chap---------BL**](a-msds-tasksforazrolebl.md)                  | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**ms DS-工作--Az-Task-BL**](a-msds-tasksforaztaskbl.md)                  | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**Ms-exch-assistant-name-擁有者-BL**](a-ownerbl.md)                                          | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**msSFU-30-Posix-成員**](a-mssfu30posixmemberof.md)                     | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**netboot-SCP-BL**](a-netbootscpbl.md)                                       | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**非安全性成員-BL**](a-nonsecuritymemberbl.md)                        | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**NT-Security-描述元**](a-ntsecuritydescriptor.md)                       | 是      | [**返回頁首**](c-top.md)<br/>                                       |
| [**Obj-Dist 名稱**](a-distinguishedname.md)                                   | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**物件-類別**](a-objectcategory.md)                                    | 是      | [**返回頁首**](c-top.md)<br/>                                       |
| [**物件類別**](a-objectclass.md)                                          | 是      | [**返回頁首**](c-top.md)<br/>                                       |
| [**物件-Guid**](a-objectguid.md)                                            | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**物件版本**](a-objectversion.md)                                      | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**組織單位-名稱**](a-ou.md)                                       | 否     | **居住人**                                                |
| [**其他知名物件**](a-otherwellknownobjects.md)                    | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**部分屬性-刪除-清單**](a-partialattributedeletionlist.md)      | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**部分屬性集**](a-partialattributeset.md)                         | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**實體傳遞-Office-名稱**](a-physicaldeliveryofficename.md)          | 否     | **居住人**                                                |
| [**可能-Inferiors**](a-possibleinferiors.md)                              | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**郵件標籤**](a-postaladdress.md)                                      | 否     | **居住人**                                                |
| [**郵遞區號**](a-postalcode.md)                                            | 否     | **居住人**                                                |
| [**後續 Office-Box**](a-postofficebox.md)                                     | 否     | **居住人**                                                |
| [**慣用傳遞方法**](a-preferreddeliverymethod.md)                 | 否     | **居住人**                                                |
| [**Proxy-物件名稱**](a-proxiedobjectname.md)                             | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**Proxy 位址**](a-proxyaddresses.md)                                    | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**查詢-原則-BL**](a-querypolicybl.md)                                     | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**RDN**](a-name.md)                                                          | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**登入位址**](a-registeredaddress.md)                              | 否     | **居住人**                                                |
| [**複寫-屬性中繼資料**](a-replpropertymetadata.md)                      | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**複寫-UpToDate-向量**](a-repluptodatevector.md)                           | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**報表**](a-directreports.md)                                             | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**代表-來源**](a-repsfrom.md)                                                | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**代表**](a-repsto.md)                                                    | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**修訂**](a-revision.md)                                                 | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**SD-Rights-有效**](a-sdrightseffective.md)                             | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**請參閱-也**](a-seealso.md)                                                  | 否     | [**人**](c-person.md)<br/>                                 |
| [**序號**](a-serialnumber.md)                                        | 否     | [**人**](c-person.md)<br/>                                 |
| [**伺服器參考-BL**](a-serverreferencebl.md)                             | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**顯示-內建-僅限視圖**](a-showinadvancedviewonly.md)                 | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**網站-物件-BL**](a-siteobjectbl.md)                                       | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**州/省名稱**](a-st.md)                                         | 否     | **居住人**                                                |
| [**街道位址**](a-street.md)                                             | 否     | **居住人**                                                |
| [**結構物件類別**](a-structuralobjectclass.md)                     | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**子 Refs**](a-subrefs.md)                                                  | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                               | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**姓**](a-sn.md)                                                        | 否     | [**人**](c-person.md)<br/>                                 |
| [**系統旗標**](a-systemflags.md)                                          | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**電話號碼**](a-telephonenumber.md)                                  | 否     | [**人**](c-person.md)<br/>                                 |
| [**Teletex-終端機-識別碼**](a-teletexterminalidentifier.md)             | 否     | **居住人**                                                |
| [**電傳號碼**](a-telexnumber.md)                                          | 否     | **居住人**                                                |
| [**標題**](a-title.md)                                                       | 否     | **居住人**                                                |
| [**使用者-密碼**](a-userpassword.md)                                        | 否     | [**人**](c-person.md)<br/>                                 |
| [**USN-已變更**](a-usnchanged.md)                                            | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**USN-已建立**](a-usncreated.md)                                            | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**USN-已移除-最後-Obj**](a-usndsalastobjremoved.md)                     | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**USN-站間**](a-usnintersite.md)                                        | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**USN-最後-Obj-Rem**](a-usnlastobjrem.md)                                    | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**USN-來源**](a-usnsource.md)                                              | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**Wbem-路徑**](a-wbempath.md)                                                | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**知名物件**](a-wellknownobjects.md)                               | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**變更時**](a-whenchanged.md)                                          | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**建立時間**](a-whencreated.md)                                          | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**WWW-首頁**](a-wwwhomepage.md)                                         | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**WWW-頁面-其他**](a-url.md)                                                | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**X121-位址**](a-x121address.md)                                          | 否     | **居住人**                                                |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2

-   [屬性](#windows-server-2008-r2-attributes)



| 進入 | 值 |
|-----------------------------|----------------------------------------------------------------------------------------------|
| System-Only                 | 否                                                                                        |
| Object-Category             | 1                                                                                            |
| 預設-物件-類別     | \-                                                                                           |
| Governs-Id                  | 2.5.6.10                                                                                     |
| 預設值-隱藏-值        | 1                                                                                            |
| Rdn-Att-Id                  | [**一般名稱**](a-cn.md)<br/>                                                       |
| 的子類別                 | [**人**](c-person.md)<br/>                                                        |
| 可能的 Superiors          | [**容器**](c-container.md)[**位置**](c-locality.md)                               |
| 輔助類別           | \-                                                                                           |
| NT-Security-描述元      | O:BAG：不正確： S：                                                                                 |
| 預設安全描述項 | D:(A;;RPWPCRCCDCLCLORCWOWDSDDTSW;;;DA)(A;;RPWPCRCCDCLCLORCWOWDSDDTSW;;;SY)(A;;RPLCLORC;;;AU) |
| System-Flags                | 0x00000010                                                                                   |



## <a name="windows-server-2008-r2-attributes"></a>WindowsServer 2008 R2 屬性

此類別包含 Windows Server 2008 R2 的下列屬性：



| 屬性                                                                        | 強制性 | 衍生自                                                          |
|----------------------------------------------------------------------------------|-----------|-----------------------------------------------------------------------|
| [**系統管理員-描述**](a-admindescription.md)                                  | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**系統管理員-顯示名稱**](a-admindisplayname.md)                                 | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**允許-屬性**](a-allowedattributes.md)                                | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**允許-屬性-有效**](a-allowedattributeseffective.md)             | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**允許-子類別**](a-allowedchildclasses.md)                           | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**允許-子類別-有效**](a-allowedchildclasseseffective.md)        | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**attributeCertificateAttribute**](a-attributecertificateattribute.md)         | 否     | [**人**](c-person.md)<br/>                                 |
| [**橋頭-伺服器-清單-BL**](a-bridgeheadserverlistbl.md)                    | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**商務-類別**](a-businesscategory.md)                                  | 否     | **居住人**                                                |
| [**標準名稱**](a-canonicalname.md)                                        | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**一般名稱**](a-cn.md)                                                      | 是      | [**人**](c-person.md)<br/> [**返回頁首**](c-top.md)<br/> |
| [**建立時間戳記**](a-createtimestamp.md)                                   | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**描述**](a-description.md)                                             | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**目的地-指標**](a-destinationindicator.md)                          | 否     | **居住人**                                                |
| [**顯示名稱**](a-displayname.md)                                            | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**顯示-名稱-可列印**](a-displaynameprintable.md)                         | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**DSA-簽章**](a-dsasignature.md)                                          | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**DS-核心-傳播-資料**](a-dscorepropagationdata.md)                      | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**副檔名-名稱**](a-extensionname.md)                                        | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**傳真-電話號碼**](a-facsimiletelephonenumber.md)                 | 否     | **居住人**                                                |
| [**標誌**](a-flags.md)                                                         | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**從-進入**](a-fromentry.md)                                                | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**Frs-電腦-參考-BL**](a-frscomputerreferencebl.md)                    | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**FRS-成員參考-BL**](a-frsmemberreferencebl.md)                        | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**FSMO 角色-擁有者**](a-fsmoroleowner.md)                                       | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**實例類型**](a-instancetype.md)                                          | 是      | [**返回頁首**](c-top.md)<br/>                                       |
| [**國際 ISDN 號碼**](a-internationalisdnnumber.md)                   | 否     | **居住人**                                                |
| [**為關鍵-系統物件**](a-iscriticalsystemobject.md)                    | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**已刪除**](a-isdeleted.md)                                                | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**是-DL 的成員**](a-memberof.md)                                            | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**是-許可權-持有者**](a-isprivilegeholder.md)                               | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**已回收**](a-isrecycled.md)                                              | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**最後一個已知-父系**](a-lastknownparent.md)                                   | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**位置名稱**](a-l.md)                                                     | 否     | **居住人**                                                |
| [**Managed 物件**](a-managedobjects.md)                                      | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**主要**](a-masteredby.md)                                              | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**修改時間戳記**](a-modifytimestamp.md)                                   | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**PartitionSetLink**](a-mscom-partitionsetlink.md)                      | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**UserLink**](a-mscom-userlink.md)                                      | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**ms-DFSR-ComputerReferenceBL**](a-msdfsr-computerreferencebl.md)              | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**ms-DFSR-MemberReferenceBL**](a-msdfsr-memberreferencebl.md)                  | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**ms-DS-Immed-從屬**](a-msds-approx-immed-subordinates.md)      | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**ms-DS-AuthenticatedTo-Accountlist**](a-msds-authenticatedtoaccountlist.md)   | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**MS DS-一致性-子計數**](a-ms-ds-consistencychildcount.md)           | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                        | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**啟用 ms DS-功能-BL**](a-msds-enabledfeaturebl.md)                      | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**ms-DS-服務-帳戶-BL**](a-msds-hostserviceaccountbl.md)             | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**ms-DS-Is-Domain-For**](a-msds-isdomainfor.md)                                | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**ms-DS-Is-Full-Replica-For**](a-msds-isfullreplicafor.md)                     | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**ms-chap-為部分複本**](a-msds-ispartialreplicafor.md)               | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**ms-DS-KrbTgt-連結-BL**](a-msds-krbtgtlinkbl.md)                              | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**ms-DS-最近-RDN**](a-msds-lastknownrdn.md)                              | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**ms DS-本機有效-刪除時間**](a-msds-localeffectivedeletiontime.md) | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**ms DS-本機有效-回收時間**](a-msds-localeffectiverecycletime.md)   | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**ms DS-主要-依據**](a-msds-masteredby.md)                                   | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**ms DS-成員--Az-Role-BL**](a-msds-membersforazrolebl.md)                | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**ms DS-NC-複寫-資料指標**](a-msds-ncreplcursors.md)                            | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**ms-DS-NC-複寫-輸入-相鄰**](a-msds-ncreplinboundneighbors.md)         | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**ms DS-NC-複寫-輸出-相鄰**](a-msds-ncreploutboundneighbors.md)       | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**ms DS-NC-RO-複本-位置-BL**](a-msds-nc-ro-replica-locations-bl.md)    | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**ms-DS-NC 類型**](a-msds-nctype.md)                                           | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**ms DS-非成員-BL**](a-msds-nonmembersbl.md)                              | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**BL-------物件參考**](a-msds-objectreferencebl.md)                    | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**OIDToGroup-連結-BL**](a-msds-oidtogrouplinkbl.md)                      | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**BL-------------------**](a-msds-operationsforazrolebl.md)          | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**BL-------------工作-**](a-msds-operationsforaztaskbl.md)          | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**ms-DS-主體-名稱**](a-msds-principalname.md)                             | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**PSO-已套用**](a-msds-psoapplied.md)                                   | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**ms-DS-複寫-屬性中繼資料**](a-msds-replattributemetadata.md)           | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**ms-DS-複製-值中繼資料**](a-msds-replvaluemetadata.md)                   | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**ms-DS-顯示的 Dsa**](a-msds-revealeddsas.md)                               | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**ms-DS-Revealed-List-BL**](a-msds-revealedlistbl.md)                          | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**ms-chap---------BL**](a-msds-tasksforazrolebl.md)                    | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**ms DS-工作--Az-Task-BL**](a-msds-tasksforaztaskbl.md)                    | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**Ms-exch-assistant-name-擁有者-BL**](a-ownerbl.md)                                            | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**msSFU-30-Posix-成員**](a-mssfu30posixmemberof.md)                       | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**netboot-SCP-BL**](a-netbootscpbl.md)                                         | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**非安全性成員-BL**](a-nonsecuritymemberbl.md)                          | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**NT-Security-描述元**](a-ntsecuritydescriptor.md)                         | 是      | [**返回頁首**](c-top.md)<br/>                                       |
| [**Obj-Dist 名稱**](a-distinguishedname.md)                                     | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**物件-類別**](a-objectcategory.md)                                      | 是      | [**返回頁首**](c-top.md)<br/>                                       |
| [**物件類別**](a-objectclass.md)                                            | 是      | [**返回頁首**](c-top.md)<br/>                                       |
| [**物件-Guid**](a-objectguid.md)                                              | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**物件版本**](a-objectversion.md)                                        | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**組織單位-名稱**](a-ou.md)                                         | 否     | **居住人**                                                |
| [**其他知名物件**](a-otherwellknownobjects.md)                      | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**部分屬性-刪除-清單**](a-partialattributedeletionlist.md)        | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**部分屬性集**](a-partialattributeset.md)                           | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**實體傳遞-Office-名稱**](a-physicaldeliveryofficename.md)            | 否     | **居住人**                                                |
| [**可能-Inferiors**](a-possibleinferiors.md)                                | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**郵件標籤**](a-postaladdress.md)                                        | 否     | **居住人**                                                |
| [**郵遞區號**](a-postalcode.md)                                              | 否     | **居住人**                                                |
| [**後續 Office-Box**](a-postofficebox.md)                                       | 否     | **居住人**                                                |
| [**慣用傳遞方法**](a-preferreddeliverymethod.md)                   | 否     | **居住人**                                                |
| [**Proxy-物件名稱**](a-proxiedobjectname.md)                               | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**Proxy 位址**](a-proxyaddresses.md)                                      | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**查詢-原則-BL**](a-querypolicybl.md)                                       | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**RDN**](a-name.md)                                                            | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**登入位址**](a-registeredaddress.md)                                | 否     | **居住人**                                                |
| [**複寫-屬性中繼資料**](a-replpropertymetadata.md)                        | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**複寫-UpToDate-向量**](a-repluptodatevector.md)                             | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**報表**](a-directreports.md)                                               | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**代表-來源**](a-repsfrom.md)                                                  | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**代表**](a-repsto.md)                                                      | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**修訂**](a-revision.md)                                                   | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**SD-Rights-有效**](a-sdrightseffective.md)                               | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**請參閱-也**](a-seealso.md)                                                    | 否     | [**人**](c-person.md)<br/>                                 |
| [**序號**](a-serialnumber.md)                                          | 否     | [**人**](c-person.md)<br/>                                 |
| [**伺服器參考-BL**](a-serverreferencebl.md)                               | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**顯示-內建-僅限視圖**](a-showinadvancedviewonly.md)                   | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**網站-物件-BL**](a-siteobjectbl.md)                                         | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**州/省名稱**](a-st.md)                                           | 否     | **居住人**                                                |
| [**街道位址**](a-street.md)                                               | 否     | **居住人**                                                |
| [**結構物件類別**](a-structuralobjectclass.md)                       | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**子 Refs**](a-subrefs.md)                                                    | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                                 | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**姓**](a-sn.md)                                                          | 否     | [**人**](c-person.md)<br/>                                 |
| [**系統旗標**](a-systemflags.md)                                            | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**電話號碼**](a-telephonenumber.md)                                    | 否     | [**人**](c-person.md)<br/>                                 |
| [**Teletex-終端機-識別碼**](a-teletexterminalidentifier.md)               | 否     | **居住人**                                                |
| [**電傳號碼**](a-telexnumber.md)                                            | 否     | **居住人**                                                |
| [**標題**](a-title.md)                                                         | 否     | **居住人**                                                |
| [**使用者-密碼**](a-userpassword.md)                                          | 否     | [**人**](c-person.md)<br/>                                 |
| [**USN-已變更**](a-usnchanged.md)                                              | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**USN-已建立**](a-usncreated.md)                                              | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**USN-已移除-最後-Obj**](a-usndsalastobjremoved.md)                       | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**USN-站間**](a-usnintersite.md)                                          | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**USN-最後-Obj-Rem**](a-usnlastobjrem.md)                                      | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**USN-來源**](a-usnsource.md)                                                | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**Wbem-路徑**](a-wbempath.md)                                                  | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**知名物件**](a-wellknownobjects.md)                                 | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**變更時**](a-whenchanged.md)                                            | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**建立時間**](a-whencreated.md)                                            | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**WWW-首頁**](a-wwwhomepage.md)                                           | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**WWW-頁面-其他**](a-url.md)                                                  | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**X121-位址**](a-x121address.md)                                            | 否     | **居住人**                                                |



## <a name="windows-server-2012"></a>Windows Server 2012

-   [屬性](#windows-server-2012-attributes)



| 進入 | 值 |
|-----------------------------|----------------------------------------------------------------------------------------------|
| System-Only                 | 否                                                                                        |
| Object-Category             | 1                                                                                            |
| 預設-物件-類別     | \-                                                                                           |
| Governs-Id                  | 2.5.6.10                                                                                     |
| 預設值-隱藏-值        | 1                                                                                            |
| Rdn-Att-Id                  | [**一般名稱**](a-cn.md)<br/>                                                       |
| 的子類別                 | [**人**](c-person.md)<br/>                                                        |
| 可能的 Superiors          | [**容器**](c-container.md)[**位置**](c-locality.md)                               |
| 輔助類別           | \-                                                                                           |
| NT-Security-描述元      | O:BAG：不正確： S：                                                                                 |
| 預設安全描述項 | D:(A;;RPWPCRCCDCLCLORCWOWDSDDTSW;;;DA)(A;;RPWPCRCCDCLCLORCWOWDSDDTSW;;;SY)(A;;RPLCLORC;;;AU) |
| System-Flags                | 0x00000010                                                                                   |



## <a name="windows-server-2012-attributes"></a>Windows Server 2012屬性

這個類別包含 Windows Server 2012 的下列屬性：



| 屬性                                                                                    | 強制性 | 衍生自                                                          |
|----------------------------------------------------------------------------------------------|-----------|-----------------------------------------------------------------------|
| [**系統管理員-描述**](a-admindescription.md)                                              | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**系統管理員-顯示名稱**](a-admindisplayname.md)                                             | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**允許-屬性**](a-allowedattributes.md)                                            | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**允許-屬性-有效**](a-allowedattributeseffective.md)                         | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**允許-子類別**](a-allowedchildclasses.md)                                       | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**允許-子類別-有效**](a-allowedchildclasseseffective.md)                    | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**attributeCertificateAttribute**](a-attributecertificateattribute.md)                     | 否     | [**人**](c-person.md)<br/>                                 |
| [**橋頭-伺服器-清單-BL**](a-bridgeheadserverlistbl.md)                                | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**商務-類別**](a-businesscategory.md)                                              | 否     | **居住人**                                                |
| [**標準名稱**](a-canonicalname.md)                                                    | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**一般名稱**](a-cn.md)                                                                  | 是      | [**人**](c-person.md)<br/> [**返回頁首**](c-top.md)<br/> |
| [**建立時間戳記**](a-createtimestamp.md)                                               | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**描述**](a-description.md)                                                         | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**目的地-指標**](a-destinationindicator.md)                                      | 否     | **居住人**                                                |
| [**顯示名稱**](a-displayname.md)                                                        | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**顯示-名稱-可列印**](a-displaynameprintable.md)                                     | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**DSA-簽章**](a-dsasignature.md)                                                      | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**DS-核心-傳播-資料**](a-dscorepropagationdata.md)                                  | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**副檔名-名稱**](a-extensionname.md)                                                    | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**傳真-電話號碼**](a-facsimiletelephonenumber.md)                             | 否     | **居住人**                                                |
| [**標誌**](a-flags.md)                                                                     | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**從-進入**](a-fromentry.md)                                                            | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**Frs-電腦-參考-BL**](a-frscomputerreferencebl.md)                                | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**FRS-成員參考-BL**](a-frsmemberreferencebl.md)                                    | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**FSMO 角色-擁有者**](a-fsmoroleowner.md)                                                   | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**實例類型**](a-instancetype.md)                                                      | 是      | [**返回頁首**](c-top.md)<br/>                                       |
| [**國際 ISDN 號碼**](a-internationalisdnnumber.md)                               | 否     | **居住人**                                                |
| [**為關鍵-系統物件**](a-iscriticalsystemobject.md)                                | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**已刪除**](a-isdeleted.md)                                                            | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**是-DL 的成員**](a-memberof.md)                                                        | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**是-許可權-持有者**](a-isprivilegeholder.md)                                           | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**已回收**](a-isrecycled.md)                                                          | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**最後一個已知-父系**](a-lastknownparent.md)                                               | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**位置名稱**](a-l.md)                                                                 | 否     | **居住人**                                                |
| [**Managed 物件**](a-managedobjects.md)                                                  | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**主要**](a-masteredby.md)                                                          | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**修改時間戳記**](a-modifytimestamp.md)                                               | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**PartitionSetLink**](a-mscom-partitionsetlink.md)                                  | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**UserLink**](a-mscom-userlink.md)                                                  | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**ms-DFSR-ComputerReferenceBL**](a-msdfsr-computerreferencebl.md)                          | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**ms-DFSR-MemberReferenceBL**](a-msdfsr-memberreferencebl.md)                              | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**ms-DS-Immed-從屬**](a-msds-approx-immed-subordinates.md)                  | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**ms-DS-AuthenticatedTo-Accountlist**](a-msds-authenticatedtoaccountlist.md)               | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**ms-chap--------可能-值-BL**](a-msds-claimsharespossiblevalueswithbl.md) | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**MS DS-一致性-子計數**](a-ms-ds-consistencychildcount.md)                       | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                                    | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**啟用 ms DS-功能-BL**](a-msds-enabledfeaturebl.md)                                  | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**ms-DS-服務-帳戶-BL**](a-msds-hostserviceaccountbl.md)                         | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**ms-DS-Is-Domain-For**](a-msds-isdomainfor.md)                                            | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**ms-DS-Is-Full-Replica-For**](a-msds-isfullreplicafor.md)                                 | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**ms-chap-為部分複本**](a-msds-ispartialreplicafor.md)                           | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**ms-chap---主要電腦-**](a-msds-isprimarycomputerfor.md)                         | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**ms-DS-KrbTgt-連結-BL**](a-msds-krbtgtlinkbl.md)                                          | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**ms-DS-最近-RDN**](a-msds-lastknownrdn.md)                                          | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**ms DS-本機有效-刪除時間**](a-msds-localeffectivedeletiontime.md)             | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**ms DS-本機有效-回收時間**](a-msds-localeffectiverecycletime.md)               | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**ms DS-主要-依據**](a-msds-masteredby.md)                                               | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**ms DS-成員--Az-Role-BL**](a-msds-membersforazrolebl.md)                            | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**ms-chap-資源--BL 的成員**](a-msds-membersofresourcepropertylistbl.md) | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**ms DS-NC-複寫-資料指標**](a-msds-ncreplcursors.md)                                        | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**ms-DS-NC-複寫-輸入-相鄰**](a-msds-ncreplinboundneighbors.md)                     | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**ms DS-NC-複寫-輸出-相鄰**](a-msds-ncreploutboundneighbors.md)                   | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**ms DS-NC-RO-複本-位置-BL**](a-msds-nc-ro-replica-locations-bl.md)                | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**ms-DS-NC 類型**](a-msds-nctype.md)                                                       | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**ms DS-非成員-BL**](a-msds-nonmembersbl.md)                                          | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**BL-------物件參考**](a-msds-objectreferencebl.md)                                | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**OIDToGroup-連結-BL**](a-msds-oidtogrouplinkbl.md)                                  | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**BL-------------------**](a-msds-operationsforazrolebl.md)                      | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**BL-------------工作-**](a-msds-operationsforaztaskbl.md)                      | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**ms-DS-主體-名稱**](a-msds-principalname.md)                                         | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**PSO-已套用**](a-msds-psoapplied.md)                                               | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**ms-DS-複寫-屬性中繼資料**](a-msds-replattributemetadata.md)                       | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**ms-DS-複製-值中繼資料**](a-msds-replvaluemetadata.md)                               | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**ms-DS-顯示的 Dsa**](a-msds-revealeddsas.md)                                           | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**ms-DS-Revealed-List-BL**](a-msds-revealedlistbl.md)                                      | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**ms-chap---------BL**](a-msds-tasksforazrolebl.md)                                | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**ms DS-工作--Az-Task-BL**](a-msds-tasksforaztaskbl.md)                                | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**ms-chap-Egress-BL**](a-msds-tdoegressbl.md)                                            | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**ms-DS-TDO-輸入-BL**](a-msds-tdoingressbl.md)                                          | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**ms-chap-------Reference-BL**](a-msds-valuetypereferencebl.md)                         | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**Ms-exch-assistant-name-擁有者-BL**](a-ownerbl.md)                                                        | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**msSFU-30-Posix-成員**](a-mssfu30posixmemberof.md)                                   | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**netboot-SCP-BL**](a-netbootscpbl.md)                                                     | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**非安全性成員-BL**](a-nonsecuritymemberbl.md)                                      | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**NT-Security-描述元**](a-ntsecuritydescriptor.md)                                     | 是      | [**返回頁首**](c-top.md)<br/>                                       |
| [**Obj-Dist 名稱**](a-distinguishedname.md)                                                 | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**物件-類別**](a-objectcategory.md)                                                  | 是      | [**返回頁首**](c-top.md)<br/>                                       |
| [**物件類別**](a-objectclass.md)                                                        | 是      | [**返回頁首**](c-top.md)<br/>                                       |
| [**物件-Guid**](a-objectguid.md)                                                          | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**物件版本**](a-objectversion.md)                                                    | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**組織單位-名稱**](a-ou.md)                                                     | 否     | **居住人**                                                |
| [**其他知名物件**](a-otherwellknownobjects.md)                                  | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**部分屬性-刪除-清單**](a-partialattributedeletionlist.md)                    | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**部分屬性集**](a-partialattributeset.md)                                       | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**實體傳遞-Office-名稱**](a-physicaldeliveryofficename.md)                        | 否     | **居住人**                                                |
| [**可能-Inferiors**](a-possibleinferiors.md)                                            | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**郵件標籤**](a-postaladdress.md)                                                    | 否     | **居住人**                                                |
| [**郵遞區號**](a-postalcode.md)                                                          | 否     | **居住人**                                                |
| [**後續 Office-Box**](a-postofficebox.md)                                                   | 否     | **居住人**                                                |
| [**慣用傳遞方法**](a-preferreddeliverymethod.md)                               | 否     | **居住人**                                                |
| [**Proxy-物件名稱**](a-proxiedobjectname.md)                                           | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**Proxy 位址**](a-proxyaddresses.md)                                                  | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**查詢-原則-BL**](a-querypolicybl.md)                                                   | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**RDN**](a-name.md)                                                                        | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**登入位址**](a-registeredaddress.md)                                            | 否     | **居住人**                                                |
| [**複寫-屬性中繼資料**](a-replpropertymetadata.md)                                    | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**複寫-UpToDate-向量**](a-repluptodatevector.md)                                         | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**報表**](a-directreports.md)                                                           | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**代表-來源**](a-repsfrom.md)                                                              | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**代表**](a-repsto.md)                                                                  | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**修訂**](a-revision.md)                                                               | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**SD-Rights-有效**](a-sdrightseffective.md)                                           | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**請參閱-也**](a-seealso.md)                                                                | 否     | [**人**](c-person.md)<br/>                                 |
| [**序號**](a-serialnumber.md)                                                      | 否     | [**人**](c-person.md)<br/>                                 |
| [**伺服器參考-BL**](a-serverreferencebl.md)                                           | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**顯示-內建-僅限視圖**](a-showinadvancedviewonly.md)                               | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**網站-物件-BL**](a-siteobjectbl.md)                                                     | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**州/省名稱**](a-st.md)                                                       | 否     | **居住人**                                                |
| [**街道位址**](a-street.md)                                                           | 否     | **居住人**                                                |
| [**結構物件類別**](a-structuralobjectclass.md)                                   | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**子 Refs**](a-subrefs.md)                                                                | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                                             | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**姓**](a-sn.md)                                                                      | 否     | [**人**](c-person.md)<br/>                                 |
| [**系統旗標**](a-systemflags.md)                                                        | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**電話號碼**](a-telephonenumber.md)                                                | 否     | [**人**](c-person.md)<br/>                                 |
| [**Teletex-終端機-識別碼**](a-teletexterminalidentifier.md)                           | 否     | **居住人**                                                |
| [**電傳號碼**](a-telexnumber.md)                                                        | 否     | **居住人**                                                |
| [**標題**](a-title.md)                                                                     | 否     | **居住人**                                                |
| [**使用者-密碼**](a-userpassword.md)                                                      | 否     | [**人**](c-person.md)<br/>                                 |
| [**USN-已變更**](a-usnchanged.md)                                                          | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**USN-已建立**](a-usncreated.md)                                                          | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**USN-已移除-最後-Obj**](a-usndsalastobjremoved.md)                                   | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**USN-站間**](a-usnintersite.md)                                                      | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**USN-最後-Obj-Rem**](a-usnlastobjrem.md)                                                  | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**USN-來源**](a-usnsource.md)                                                            | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**Wbem-路徑**](a-wbempath.md)                                                              | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**知名物件**](a-wellknownobjects.md)                                             | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**變更時**](a-whenchanged.md)                                                        | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**建立時間**](a-whencreated.md)                                                        | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**WWW-首頁**](a-wwwhomepage.md)                                                       | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**WWW-頁面-其他**](a-url.md)                                                              | 否     | [**返回頁首**](c-top.md)<br/>                                       |
| [**X121-位址**](a-x121address.md)                                                        | 否     | **居住人**                                                |



 

 





