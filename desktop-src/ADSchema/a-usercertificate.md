---
title: X509-Cert 屬性
description: 包含發給使用者的 DER 編碼 x.509v3 憑證。 請注意，此屬性包含由 Microsoft 憑證服務發給此使用者的公開金鑰憑證。
ms.assetid: bdd6b9a4-c402-462c-be2c-8e7e582a899a
ms.tgt_platform: multiple
keywords:
- X509-Cert 屬性 AD 架構
- userCertificate 屬性 AD 架構
topic_type:
- apiref
api_name:
- X509-Cert
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: faa6f0dfb5acc25890361a124e52b8b24958915f
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "104467312"
---
# <a name="x509-cert-attribute"></a>X509-Cert 屬性

包含發給使用者的 DER 編碼 x.509v3 憑證。 請注意，此屬性包含由 Microsoft 憑證服務發給此使用者的公開金鑰憑證。



| 進入 | 值 |
|-------------------|-------------------------------------------------------------------------------------------------------------------------|
| CN                | X509-Cert                                                                                                               |
| Ldap-顯示名稱 | userCertificate                                                                                                         |
| 大小              | 針對每個使用 KRA 實例的 CA 所發出的金鑰復原代理憑證，此屬性將需要大約 4 KB。 |
| 更新許可權  | 網域系統管理員                                                                                                    |
| 更新頻率  | 每次發行憑證時。                                                                                      |
| Attribute-Id      | 2.5.4.36                                                                                                                |
| 系統識別碼-Guid    | bf967a7f-0de6-11d0-a285-00aa003049e2                                                                                    |
| Syntax            | [**Object(Replica-Link)**](s-object-replica-link.md)                                                                   |



## <a name="implementations"></a>實作

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| 進入 | 值 |
|------------------------|----------------------------------------------------------------------------------------|
| 連結識別碼                | \-                                                                                     |
| MAPI-Id                | 0x8C6A                                                                                 |
| System-Only            | 否                                                                                  |
| 是-單一值       | 否                                                                                  |
| 已編制索引             | 否                                                                                  |
| 在通用類別目錄中      | 對                                                                                   |
| NT-Security-描述元 | O:BAG：不正確： S：                                                                           |
| Range-Lower            | \-                                                                                     |
| Range-Upper            | \-                                                                                     |
| Search-Flags           | 0x00000000                                                                             |
| System-Flags           | 0x00000010                                                                             |
| 中使用的類別        | [**郵件收件者**](c-mailrecipient.md)<br/> [**User**](c-user.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| 進入 | 值 |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 連結識別碼                | \-                                                                                                                                                                                                                                 |
| MAPI-Id                | 0x8C6A                                                                                                                                                                                                                             |
| System-Only            | 否                                                                                                                                                                                                                              |
| 是-單一值       | 否                                                                                                                                                                                                                              |
| 已編制索引             | 否                                                                                                                                                                                                                              |
| 在通用類別目錄中      | 對                                                                                                                                                                                                                               |
| NT-Security-描述元 | O:BAG：不正確： S：                                                                                                                                                                                                                       |
| Range-Lower            | \-                                                                                                                                                                                                                                 |
| Range-Upper            | \-                                                                                                                                                                                                                                 |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                         |
| System-Flags           | 0x00000010                                                                                                                                                                                                                         |
| 中使用的類別        | [**inetOrgPerson**](c-inetorgperson.md)<br/> [**郵件收件者**](c-mailrecipient.md)<br/> [**ms-PKI-私用金鑰-復原代理程式**](c-mspki-privatekeyrecoveryagent.md)<br/> [**User**](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| 進入 | 值 |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 連結識別碼                | \-                                                                                                                                                                                                                                 |
| MAPI-Id                | 0x8C6A                                                                                                                                                                                                                             |
| System-Only            | 否                                                                                                                                                                                                                              |
| 是-單一值       | 否                                                                                                                                                                                                                              |
| 已編制索引             | 否                                                                                                                                                                                                                              |
| 在通用類別目錄中      | 對                                                                                                                                                                                                                               |
| NT-Security-描述元 | O:BAG：不正確： S：                                                                                                                                                                                                                       |
| Range-Lower            | \-                                                                                                                                                                                                                                 |
| Range-Upper            | \-                                                                                                                                                                                                                                 |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                         |
| System-Flags           | 0x00000010                                                                                                                                                                                                                         |
| 中使用的類別        | [**inetOrgPerson**](c-inetorgperson.md)<br/> [**郵件收件者**](c-mailrecipient.md)<br/> [**ms-PKI-私用金鑰-復原代理程式**](c-mspki-privatekeyrecoveryagent.md)<br/> [**User**](c-user.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| 進入 | 值 |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 連結識別碼                | \-                                                                                                                                                                                                                                 |
| MAPI-Id                | 0x8C6A                                                                                                                                                                                                                             |
| System-Only            | 否                                                                                                                                                                                                                              |
| 是-單一值       | 否                                                                                                                                                                                                                              |
| 已編制索引             | 否                                                                                                                                                                                                                              |
| 在通用類別目錄中      | 對                                                                                                                                                                                                                               |
| NT-Security-描述元 | O:BAG：不正確： S：                                                                                                                                                                                                                       |
| Range-Lower            | \-                                                                                                                                                                                                                                 |
| Range-Upper            | \-                                                                                                                                                                                                                                 |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                         |
| System-Flags           | 0x00000010                                                                                                                                                                                                                         |
| 中使用的類別        | [**inetOrgPerson**](c-inetorgperson.md)<br/> [**郵件收件者**](c-mailrecipient.md)<br/> [**ms-PKI-私用金鑰-復原代理程式**](c-mspki-privatekeyrecoveryagent.md)<br/> [**User**](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| 進入 | 值 |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 連結識別碼                | \-                                                                                                                                                                                                                                 |
| MAPI-Id                | 0x8C6A                                                                                                                                                                                                                             |
| System-Only            | 否                                                                                                                                                                                                                              |
| 是-單一值       | 否                                                                                                                                                                                                                              |
| 已編制索引             | 否                                                                                                                                                                                                                              |
| 在通用類別目錄中      | 對                                                                                                                                                                                                                               |
| NT-Security-描述元 | O:BAG：不正確： S：                                                                                                                                                                                                                       |
| Range-Lower            | \-                                                                                                                                                                                                                                 |
| Range-Upper            | \-                                                                                                                                                                                                                                 |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                         |
| System-Flags           | 0x00000010                                                                                                                                                                                                                         |
| 中使用的類別        | [**inetOrgPerson**](c-inetorgperson.md)<br/> [**郵件收件者**](c-mailrecipient.md)<br/> [**ms-PKI-私用金鑰-復原代理程式**](c-mspki-privatekeyrecoveryagent.md)<br/> [**User**](c-user.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| 進入 | 值 |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 連結識別碼                | \-                                                                                                                                                                                                                                 |
| MAPI-Id                | 0x8C6A                                                                                                                                                                                                                             |
| System-Only            | 否                                                                                                                                                                                                                              |
| 是-單一值       | 否                                                                                                                                                                                                                              |
| 已編制索引             | 否                                                                                                                                                                                                                              |
| 在通用類別目錄中      | 對                                                                                                                                                                                                                               |
| NT-Security-描述元 | O:BAG：不正確： S：                                                                                                                                                                                                                       |
| Range-Lower            | \-                                                                                                                                                                                                                                 |
| Range-Upper            | \-                                                                                                                                                                                                                                 |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                         |
| System-Flags           | 0x00000010                                                                                                                                                                                                                         |
| 中使用的類別        | [**inetOrgPerson**](c-inetorgperson.md)<br/> [**郵件收件者**](c-mailrecipient.md)<br/> [**ms-PKI-私用金鑰-復原代理程式**](c-mspki-privatekeyrecoveryagent.md)<br/> [**User**](c-user.md)<br/> |



 

 





