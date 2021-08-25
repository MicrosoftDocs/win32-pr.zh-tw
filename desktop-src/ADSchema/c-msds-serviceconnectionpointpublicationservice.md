---
title: ms-DS-服務-連接點-發行集-服務類別
description: 儲存 ADAM 中服務連接點發行服務的設定選項。
ms.assetid: 30b4df70-a03b-4d42-b200-75bfa6cf8273
ms.tgt_platform: multiple
keywords:
- ms-DS-服務-連接點-發行集-服務類別 AD 架構
- ServiceConnectionPointPublicationService 類別 AD 架構
topic_type:
- apiref
api_name:
- ms-DS-Service-Connection-Point-Publication-Service
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 13b458a5d66d8d6fd90a58519ce57de03f625087be4123f2e51ca8c09534ed96
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119879838"
---
# <a name="ms-ds-service-connection-point-publication-service-class"></a>ms-DS-服務-連接點-發行集-服務類別

儲存 ADAM 中服務連接點發行服務的設定選項。



| 進入 | 值 |
|-------------------|----------------------------------------------------|
| CN                | ms-DS-服務-連接點-發行集-服務 |
| Ldap-顯示名稱 | ServiceConnectionPointPublicationService      |
| 更新許可權  | \-                                                 |
| 更新頻率  | \-                                                 |
| 架構識別碼-Guid    | d33f5da6-b009-7e48-8268-b2305529e933               |



## <a name="implementations"></a>實作

-   [**亞當**](#adam-attributes)

## <a name="adam"></a>亞當

-   [屬性](#adam-attributes)



| 進入 | 值 |
|-----------------------------|----------------------------------------|
| System-Only                 | 是                                   |
| Object-Category             | 1                                      |
| 預設-物件-類別     | \-                                     |
| Governs-Id                  | 1.2.840.113556.1.5.247                 |
| 預設值-隱藏-值        | 1                                      |
| Rdn-Att-Id                  | [**一般名稱**](a-cn.md)<br/> |
| 的子類別                 | [**返回頁首**](c-top.md)<br/>        |
| 可能的 Superiors          | [**NTDS 服務**](c-ntdsservice.md)  |
| 輔助類別           | \-                                     |
| NT-Security-描述元      | O:BAG：不正確： S：                           |
| 預設安全描述項 | D:S:                                   |
| System-Flags                | 0x00000000                             |



## <a name="adam-attributes"></a>ADAM 屬性

此類別包含 ADAM 的下列屬性：



| 屬性                                                                   | 強制性 | 衍生自                                           |
|-----------------------------------------------------------------------------|-----------|--------------------------------------------------------|
| [**系統管理員-描述**](a-admindescription.md)                             | 否     | [**返回頁首**](c-top.md)<br/>                        |
| [**系統管理員-顯示名稱**](a-admindisplayname.md)                            | 否     | [**返回頁首**](c-top.md)<br/>                        |
| [**允許-屬性**](a-allowedattributes.md)                           | 否     | [**返回頁首**](c-top.md)<br/>                        |
| [**允許-屬性-有效**](a-allowedattributeseffective.md)        | 否     | [**返回頁首**](c-top.md)<br/>                        |
| [**允許-子類別**](a-allowedchildclasses.md)                      | 否     | [**返回頁首**](c-top.md)<br/>                        |
| [**允許-子類別-有效**](a-allowedchildclasseseffective.md)   | 否     | [**返回頁首**](c-top.md)<br/>                        |
| [**橋頭-伺服器-清單-BL**](a-bridgeheadserverlistbl.md)               | 否     | [**返回頁首**](c-top.md)<br/>                        |
| [**標準名稱**](a-canonicalname.md)                                   | 否     | [**返回頁首**](c-top.md)<br/>                        |
| [**一般名稱**](a-cn.md)                                                 | 否     | [**返回頁首**](c-top.md)<br/>                        |
| [**建立時間戳記**](a-createtimestamp.md)                              | 否     | [**返回頁首**](c-top.md)<br/>                        |
| [**描述**](a-description.md)                                        | 否     | [**返回頁首**](c-top.md)<br/>                        |
| [**顯示名稱**](a-displayname.md)                                       | 否     | [**返回頁首**](c-top.md)<br/>                        |
| [**DSA-簽章**](a-dsasignature.md)                                     | 否     | [**返回頁首**](c-top.md)<br/>                        |
| [**DS-核心-傳播-資料**](a-dscorepropagationdata.md)                 | 否     | [**返回頁首**](c-top.md)<br/>                        |
| [**啟用**](a-enabled.md)                                                | 否     | **ms-DS-服務-連接點-發行集-服務** |
| [**從-進入**](a-fromentry.md)                                           | 否     | [**返回頁首**](c-top.md)<br/>                        |
| [**FSMO 角色-擁有者**](a-fsmoroleowner.md)                                  | 否     | [**返回頁首**](c-top.md)<br/>                        |
| [**實例類型**](a-instancetype.md)                                     | 是      | [**返回頁首**](c-top.md)<br/>                        |
| [**為關鍵-系統物件**](a-iscriticalsystemobject.md)               | 否     | [**返回頁首**](c-top.md)<br/>                        |
| [**已刪除**](a-isdeleted.md)                                           | 否     | [**返回頁首**](c-top.md)<br/>                        |
| [**是-DL 的成員**](a-memberof.md)                                       | 否     | [**返回頁首**](c-top.md)<br/>                        |
| [**關鍵字**](a-keywords.md)                                              | 否     | **ms-DS-服務-連接點-發行集-服務** |
| [**最後一個已知-父系**](a-lastknownparent.md)                              | 否     | [**返回頁首**](c-top.md)<br/>                        |
| [**Managed 物件**](a-managedobjects.md)                                 | 否     | [**返回頁首**](c-top.md)<br/>                        |
| [**主要**](a-masteredby.md)                                         | 否     | [**返回頁首**](c-top.md)<br/>                        |
| [**修改時間戳記**](a-modifytimestamp.md)                              | 否     | [**返回頁首**](c-top.md)<br/>                        |
| [**ms-DS-Immed-從屬**](a-msds-approx-immed-subordinates.md) | 否     | [**返回頁首**](c-top.md)<br/>                        |
| [**MS DS-一致性-子計數**](a-ms-ds-consistencychildcount.md)      | 否     | [**返回頁首**](c-top.md)<br/>                        |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                   | 否     | [**返回頁首**](c-top.md)<br/>                        |
| [**ms DS-停用-實例**](a-msds-disableforinstances.md)           | 否     | **ms-DS-服務-連接點-發行集-服務** |
| [**ms-DS-停用-實例-BL**](a-msds-disableforinstancesbl.md)      | 否     | [**返回頁首**](c-top.md)<br/>                        |
| [**ms DS-主要-依據**](a-msds-masteredby.md)                              | 否     | [**返回頁首**](c-top.md)<br/>                        |
| [**ms DS-NC-複寫-資料指標**](a-msds-ncreplcursors.md)                       | 否     | [**返回頁首**](c-top.md)<br/>                        |
| [**ms-DS-NC-複寫-輸入-相鄰**](a-msds-ncreplinboundneighbors.md)    | 否     | [**返回頁首**](c-top.md)<br/>                        |
| [**ms DS-NC-複寫-輸出-相鄰**](a-msds-ncreploutboundneighbors.md)  | 否     | [**返回頁首**](c-top.md)<br/>                        |
| [**ms-DS-複寫-屬性中繼資料**](a-msds-replattributemetadata.md)      | 否     | [**返回頁首**](c-top.md)<br/>                        |
| [**ms-DS-複製-值中繼資料**](a-msds-replvaluemetadata.md)              | 否     | [**返回頁首**](c-top.md)<br/>                        |
| [**ms-DS-SCP-容器**](a-msds-scpcontainer.md)                          | 否     | **ms-DS-服務-連接點-發行集-服務** |
| [**ms-DS-服務-帳戶-BL**](a-msds-serviceaccountbl.md)                 | 否     | [**返回頁首**](c-top.md)<br/>                        |
| [**NT-Security-描述元**](a-ntsecuritydescriptor.md)                    | 是      | [**返回頁首**](c-top.md)<br/>                        |
| [**Obj-Dist 名稱**](a-distinguishedname.md)                                | 否     | [**返回頁首**](c-top.md)<br/>                        |
| [**物件-類別**](a-objectcategory.md)                                 | 是      | [**返回頁首**](c-top.md)<br/>                        |
| [**物件類別**](a-objectclass.md)                                       | 是      | [**返回頁首**](c-top.md)<br/>                        |
| [**物件-Guid**](a-objectguid.md)                                         | 否     | [**返回頁首**](c-top.md)<br/>                        |
| [**物件版本**](a-objectversion.md)                                   | 否     | [**返回頁首**](c-top.md)<br/>                        |
| [**其他知名物件**](a-otherwellknownobjects.md)                 | 否     | [**返回頁首**](c-top.md)<br/>                        |
| [**部分屬性-刪除-清單**](a-partialattributedeletionlist.md)   | 否     | [**返回頁首**](c-top.md)<br/>                        |
| [**部分屬性集**](a-partialattributeset.md)                      | 否     | [**返回頁首**](c-top.md)<br/>                        |
| [**可能-Inferiors**](a-possibleinferiors.md)                           | 否     | [**返回頁首**](c-top.md)<br/>                        |
| [**Proxy-物件名稱**](a-proxiedobjectname.md)                          | 否     | [**返回頁首**](c-top.md)<br/>                        |
| [**Proxy 位址**](a-proxyaddresses.md)                                 | 否     | [**返回頁首**](c-top.md)<br/>                        |
| [**查詢-原則-BL**](a-querypolicybl.md)                                  | 否     | [**返回頁首**](c-top.md)<br/>                        |
| [**RDN**](a-name.md)                                                       | 否     | [**返回頁首**](c-top.md)<br/>                        |
| [**複寫-屬性中繼資料**](a-replpropertymetadata.md)                   | 否     | [**返回頁首**](c-top.md)<br/>                        |
| [**複寫-UpToDate-向量**](a-repluptodatevector.md)                        | 否     | [**返回頁首**](c-top.md)<br/>                        |
| [**代表-來源**](a-repsfrom.md)                                             | 否     | [**返回頁首**](c-top.md)<br/>                        |
| [**代表**](a-repsto.md)                                                 | 否     | [**返回頁首**](c-top.md)<br/>                        |
| [**修訂**](a-revision.md)                                              | 否     | [**返回頁首**](c-top.md)<br/>                        |
| [**SD-Rights-有效**](a-sdrightseffective.md)                          | 否     | [**返回頁首**](c-top.md)<br/>                        |
| [**伺服器參考-BL**](a-serverreferencebl.md)                          | 否     | [**返回頁首**](c-top.md)<br/>                        |
| [**顯示-內建-僅限視圖**](a-showinadvancedviewonly.md)              | 否     | [**返回頁首**](c-top.md)<br/>                        |
| [**網站-物件-BL**](a-siteobjectbl.md)                                    | 否     | [**返回頁首**](c-top.md)<br/>                        |
| [**結構物件類別**](a-structuralobjectclass.md)                  | 否     | [**返回頁首**](c-top.md)<br/>                        |
| [**子 Refs**](a-subrefs.md)                                               | 否     | [**返回頁首**](c-top.md)<br/>                        |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                            | 否     | [**返回頁首**](c-top.md)<br/>                        |
| [**系統旗標**](a-systemflags.md)                                       | 否     | [**返回頁首**](c-top.md)<br/>                        |
| [**USN-已變更**](a-usnchanged.md)                                         | 否     | [**返回頁首**](c-top.md)<br/>                        |
| [**USN-已建立**](a-usncreated.md)                                         | 否     | [**返回頁首**](c-top.md)<br/>                        |
| [**USN-已移除-最後-Obj**](a-usndsalastobjremoved.md)                  | 否     | [**返回頁首**](c-top.md)<br/>                        |
| [**USN-站間**](a-usnintersite.md)                                     | 否     | [**返回頁首**](c-top.md)<br/>                        |
| [**USN-最後-Obj-Rem**](a-usnlastobjrem.md)                                 | 否     | [**返回頁首**](c-top.md)<br/>                        |
| [**USN-來源**](a-usnsource.md)                                           | 否     | [**返回頁首**](c-top.md)<br/>                        |
| [**Wbem-路徑**](a-wbempath.md)                                             | 否     | [**返回頁首**](c-top.md)<br/>                        |
| [**知名物件**](a-wellknownobjects.md)                            | 否     | [**返回頁首**](c-top.md)<br/>                        |
| [**變更時**](a-whenchanged.md)                                       | 否     | [**返回頁首**](c-top.md)<br/>                        |
| [**建立時間**](a-whencreated.md)                                       | 否     | [**返回頁首**](c-top.md)<br/>                        |
| [**WWW-首頁**](a-wwwhomepage.md)                                      | 否     | [**返回頁首**](c-top.md)<br/>                        |
| [**WWW-頁面-其他**](a-url.md)                                             | 否     | [**返回頁首**](c-top.md)<br/>                        |



 

 





