---
title: 'RootDSE (AD 架構) '
description: 在 LDAP 3.0 中，會將 rootDSE 定義為目錄伺服器上目錄資料樹狀結構的根目錄。
ms.assetid: dd5a160d-6604-43ca-878c-6b19e90d3adb
ms.tgt_platform: multiple
keywords:
- rootDSE Active Directory 架構
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f925102904125dc781e742a3572f6b3d898eba58f8e12966f457e49b37e9f91a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119530798"
---
# <a name="rootdse-ad-schema"></a>RootDSE (AD 架構) 

在 LDAP 3.0 中，會將 rootDSE 定義為目錄伺服器上目錄資料樹狀結構的根目錄。 RootDSE 不是任何命名空間的一部分。 RootDSE 的目的是要提供目錄伺服器的相關資料。 如需有關 rootDSE 的詳細資訊，請參閱 Active Directory SDK 檔集中的 [無伺服器系結和 rootDSE](/windows/desktop/AD/serverless-binding-and-rootdse) 。

rootDSE 包含下列屬性。 除非另有說明，否則所有屬性都是單一值。



| 屬性                                    | 語法                                                 | 描述                                                                                                                                                                                                                                                                                                                                                                                                            |
|----------------------------------------------|--------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **configurationNamingCoNtext**<br/>    | [**String(Teletex)**](s-string-teletex.md)<br/> | 包含設定容器的分辨名稱。<br/>                                                                                                                                                                                                                                                                                                                                            |
| **currentTime**<br/>                   | [**String(Teletex)**](s-string-teletex.md)<br/> | 包含此目錄伺服器上以國際標準時間格式設定的目前時間。<br/>                                                                                                                                                                                                                                                                                                                |
| **defaultNamingCoNtext**<br/>          | [**String(Teletex)**](s-string-teletex.md)<br/> | 包含此目錄伺服器為其成員之網域的分辨名稱。<br/>                                                                                                                                                                                                                                                                                                                  |
| **dnsHostName**<br/>                   | [**String(Teletex)**](s-string-teletex.md)<br/> | 包含此目錄伺服器的 DNS 位址。<br/>                                                                                                                                                                                                                                                                                                                                                         |
| **domainControllerFunctionality**<br/> | [**String(Teletex)**](s-string-teletex.md)<br/> | 指出網域控制站的功能等級。 這可以是下列其中一個值。<br/> "0"-Windows 2000 模式<br/> "2"-Windows Server 2003 模式<br/> "3"-Windows Server 2008 模式<br/>                                                                                                                                                                                    |
| **domainFunctionality**<br/>           | [**String(Teletex)**](s-string-teletex.md)<br/> | 指出網域的功能等級。 這可以是下列其中一個值。<br/> "0"-Windows 2000 網域模式<br/> "1"-Windows Server 2003 過渡網域模式<br/> "2"-Windows Server 2003 網域模式<br/> "3"-Windows Server 2008 網域模式<br/> "4"-Windows Server 2008 R2 網域模式<br/>                                                             |
| **dsServiceName**<br/>                 | [**String(Teletex)**](s-string-teletex.md)<br/> | 包含此目錄伺服器之 NTDS 設定物件的分辨名稱。<br/>                                                                                                                                                                                                                                                                                                                      |
| **forestFunctionality**<br/>           | [**String(Teletex)**](s-string-teletex.md)<br/> | 指出樹系的功能等級。 這可以是下列其中一個值。<br/> "0"-Windows 2000 樹系模式<br/> "1"-Windows Server 2003 過渡樹系模式<br/> "2"-Windows Server 2003 樹系模式<br/> "3"-Windows Server 2008 樹系模式<br/> "4"-Windows Server 2008 R2 樹系模式<br/>                                                             |
| **highestCommittedUSN**<br/>           | [**String(Teletex)**](s-string-teletex.md)<br/> | 包含此目錄伺服器上 (USN) 的最高更新序號。 由目錄複寫使用。<br/>                                                                                                                                                                                                                                                                                                  |
| **isGlobalCatalogReady**<br/>          | [**String(Teletex)**](s-string-teletex.md)<br/> | 指出通用類別目錄是否可完全正常運作。 包含 "TRUE" 或 "FALSE"。<br/>                                                                                                                                                                                                                                                                                                                    |
| **System.collections.icollection.issynchronized**<br/>                | [**String(Teletex)**](s-string-teletex.md)<br/> | 指出目錄伺服器是否已完全同步處理。 包含 "TRUE" 或 "FALSE"。<br/>                                                                                                                                                                                                                                                                                                                 |
| **ldapServiceName**<br/>               | [**String(Teletex)**](s-string-teletex.md)<br/> | 包含 LDAP 伺服器 (SPN) 的服務主體名稱。 用於相互驗證。<br/>                                                                                                                                                                                                                                                                                                              |
| **namingCoNtexts**<br/>                | [**String(Teletex)**](s-string-teletex.md)<br/> | 多值屬性，其中包含儲存在此目錄伺服器上的所有命名內容的分辨名稱。 根據預設，Windows 2000 網域控制站包含至少三個命名內容：架構、設定，以及伺服器為其成員之網域的名稱。<br/>                                                                                                             |
| **rootDomainNamingCoNtext**<br/>       | [**String(Teletex)**](s-string-teletex.md)<br/> | 包含樹系中第一個網域的辨別名稱，其中包含此目錄伺服器所屬的網域。<br/>                                                                                                                                                                                                                                                                     |
| **schemaNamingCoNtext**<br/>           | [**String(Teletex)**](s-string-teletex.md)<br/> | 包含架構容器的分辨名稱。<br/>                                                                                                                                                                                                                                                                                                                                                   |
| **serverName**<br/>                    | [**String(Teletex)**](s-string-teletex.md)<br/> | 包含設定容器中此目錄伺服器之伺服器物件的分辨名稱。<br/>                                                                                                                                                                                                                                                                                             |
| **subschemaSubentry**<br/>             | [**String(Teletex)**](s-string-teletex.md)<br/> | 包含 [**ubschema**](c-subschema.md) 物件的分辨名稱。 **Ubschema** 物件包含屬性，這些屬性會在 [**objectClasses**](a-objectclasses.md)屬性) 的 [**attributeTypes**](a-attributetypes.md)屬性) 和類別 (中公開支援的屬性 (。<br/> **SubschemaSubentry** 屬性和 ubschema 是在 LDAP 3.0 中定義 (請參閱 RFC 2251) 。<br/> |
| **supportedCapabilities**<br/>         | [**String(Teletex)**](s-string-teletex.md)<br/> | 多值屬性，包含此目錄伺服器所支援的功能。<br/>                                                                                                                                                                                                                                                                                                              |
| **supportedControl**<br/>              | [**String(Teletex)**](s-string-teletex.md)<br/> | 多值屬性，包含此目錄伺服器所支援之延伸控制項的 Oid。 請參閱下表以取得可能的控制項 Oid 清單。<br/>                                                                                                                                                                                                                                  |
| **supportedLDAPPolicies**<br/>         | [**String(Teletex)**](s-string-teletex.md)<br/> | 多值屬性，其中包含支援的 LDAP 管理原則的名稱。<br/>                                                                                                                                                                                                                                                                                                              |
| **supportedLDAPVersion**<br/>          | [**String(Teletex)**](s-string-teletex.md)<br/> | 多重值的屬性，其中包含此目錄伺服器所支援) 主要版本號碼所指定的 LDAP 版本 (。<br/>                                                                                                                                                                                                                                                                         |
| **supportedSASLMechanisms**<br/>       | [**String(Teletex)**](s-string-teletex.md)<br/> | 包含支援 SASL 協商的安全性機制 (請參閱 LDAP Rfc) 。 根據預設，支援 GSSAPI。<br/>                                                                                                                                                                                                                                                                                           |



 

Active Directory 支援 **supportedControl** 屬性中的下列控制項 oid。 如需詳細資訊，請參閱 [**LDAPControl**](/previous-versions/windows/desktop/api/winldap/ns-winldap-ldapcontrola) 和 [**ldap \_ 搜尋 \_ 初始化 \_ 頁面**](/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_search_init_page)。



| 控制項 OID                        | 字串常數                                                                                   |
|------------------------------------|---------------------------------------------------------------------------------------------------|
| 1.2.840.113556.1.4.319<br/>  | [LDAP \_ 分頁 \_ 結果 \_ OID \_ 字串](/previous-versions/windows/desktop/ldap/ldap-paged-result-oid-string)<br/>                  |
| 1.2.840.113556.1.4.473<br/>  | [LDAP \_ 伺服器 \_ 排序 \_ OID](/previous-versions/windows/desktop/ldap/ldap-server-sort-oid)<br/>                                   |
| 1.2.840.113556.1.4.474<br/>  | [LDAP \_ 伺服器 \_ RESP \_ 排序 \_ OID](/previous-versions/windows/desktop/ldap/ldap-server-resp-sort-oid)<br/>                        |
| 1.2.840.113556.1.4.801<br/>  | [LDAP \_ 伺服器 \_ SD \_ FLAGS \_ OID](/previous-versions/windows/desktop/ldap/ldap-server-sd-flags-oid)<br/>                          |
| 1.2.840.113556.1.4.528<br/>  | [LDAP \_ 伺服器 \_ 通知 \_ OID](/previous-versions/windows/desktop/ldap/ldap-server-notification-oid)<br/>                   |
| 1.2.840.113556.1.4.417<br/>  | [LDAP \_ 伺服器 \_ 顯示 \_ 已刪除的 \_ OID](/previous-versions/windows/desktop/ldap/ldap-server-show-deleted-oid)<br/>                  |
| 1.2.840.113556.1.4.619<br/>  | [LDAP \_ 伺服器 \_ 延遲 \_ 認可 \_ OID](/previous-versions/windows/desktop/ldap/ldap-server-lazy-commit-oid)<br/>                    |
| 1.2.840.113556.1.4.841<br/>  | [LDAP \_ 伺服器 \_ DIRSYNC \_ OID](/previous-versions/windows/desktop/ldap/ldap-server-dirsync-oid)<br/>                             |
| 1.2.840.113556.1.4.529<br/>  | [LDAP \_ 伺服器 \_ 擴充 \_ DN \_ OID](/previous-versions/windows/desktop/ldap/ldap-server-extended-dn-oid)<br/>                    |
| 1.2.840.113556.1.4.805<br/>  | [LDAP \_ 伺服器 \_ 樹狀目錄 \_ 刪除 \_ OID](/previous-versions/windows/desktop/ldap/ldap-server-tree-delete-oid)<br/>                    |
| 1.2.840.113556.1.4.521<br/>  | [LDAP \_ 伺服器 \_ CROSSDOM \_ 移動 \_ 目標 \_ OID](/previous-versions/windows/desktop/ldap/ldap-server-crossdom-move-target-oid)<br/> |
| 1.2.840.113556.1.4.1338<br/> | [LDAP \_ 伺服器 \_ 驗證 \_ 名稱 \_ OID](/previous-versions/windows/desktop/ldap/ldap-server-verify-name-oid)<br/>                    |
| 1.2.840.113556.1.4.1339<br/> | [LDAP \_ 伺服器 \_ 網域 \_ 範圍 \_ OID](/previous-versions/windows/desktop/ldap/ldap-server-domain-scope-oid)<br/>                  |
| 1.2.840.113556.1.4.1340<br/> | [LDAP \_ 伺服器 \_ 搜尋 \_ 選項 \_ OID](/previous-versions/windows/desktop/ldap/ldap-server-search-options-oid)<br/>              |
| 1.2.840.113556.1.4.1413<br/> | [LDAP \_ 伺服器 \_ 寬鬆 \_ 修改 \_ OID](/previous-versions/windows/desktop/ldap/ldap-server-permissive-modify-oid)<br/>        |



 

 

