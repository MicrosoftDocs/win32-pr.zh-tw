---
title: Active Directory 與 LDAP 之間的資料類型對應
description: 下表將易記的語法名稱對應至對應的 LDAP 語法 OID 和 ADSTYPEENUM 值。
ms.assetid: 07952de0-0389-473a-84ca-b5f35fdc5b1f
ms.tgt_platform: multiple
keywords:
- Active Directory 與 LDAP ADSI 之間的資料類型對應
- LDAP 服務提供者 ADSI、Active Directory 與 LDAP 之間的資料類型對應
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45157fb7cefe1a993e6e16dffe28f101bc73759b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106965155"
---
# <a name="data-type-mapping-between-active-directory-and-ldap"></a>Active Directory 與 LDAP 之間的資料類型對應

下表將易記的語法名稱對應至對應的 LDAP 語法 OID 和 [**ADSTYPEENUM**](/windows/win32/api/iads/ne-iads-adstypeenum) 值。



| 易記的語法名稱              | LDAP 語法 OID               | ADSTYPEENUM 資料類型                 |
|-----------------------------------|-------------------------------|---------------------------------------|
| AccessPointDN                     | 1.3.6.1.4.1.1466.115.121.1.2  | **ADSTYPE \_ CASE \_ 忽略 \_ 字串**     |
| AttributeTypeDescription          | 1.3.6.1.4.1.1466.115.121.1.3  | **ADSTYPE \_ CASE \_ 忽略 \_ 字串**     |
| 音訊                             | 1.3.6.1.4.1.1466.115.121.1.4  | **ADSTYPE \_ 八位 \_ 字串**            |
| Binary                            | 1.3.6.1.4.1.1466.115.121.1.5  | **ADSTYPE \_ 八位 \_ 字串**            |
| BitString                         | 1.3.6.1.4.1.1466.115.121.1.6  | **ADSTYPE \_ CASE \_ 忽略 \_ 字串**     |
| Boolean                           | 1.3.6.1.4.1.1466.115.121.1.7  | **ADSTYPE \_ 布林值**                  |
| CaseExactString                   | 1.2.840.113556.1.4.1362       | **ADSTYPE \_ CASE \_ 精確 \_ 字串**      |
| CaseIgnoreString                  | 1.2.840.113556.1.4.1221       | **ADSTYPE \_ CASE \_ 忽略 \_ 字串**     |
| 憑證                       | 1.3.6.1.4.1.1466.115.121.1.8  | **ADSTYPE \_ 八位 \_ 字串**            |
| CertificateList                   | 1.3.6.1.4.1.1466.115.121.1.9  | **ADSTYPE \_ 八位 \_ 字串**            |
| CertificatePair                   | 1.3.6.1.4.1.1466.115.121.1.10 | **ADSTYPE \_ 八位 \_ 字串**            |
| 國家/地區                    | 1.3.6.1.4.1.1466.115.121.1.11 | **ADSTYPE \_ CASE \_ 忽略 \_ 字串**     |
| DataQualitySyntax                 | 1.3.6.1.4.1.1466.115.121.1.13 | **ADSTYPE \_ CASE \_ 忽略 \_ 字串**     |
| DeliveryMethod                    | 1.3.6.1.4.1.1466.115.121.1.14 | **ADSTYPE \_ CASE \_ 忽略 \_ 字串**     |
| DirectoryString                   | 1.3.6.1.4.1.1466.115.121.1.15 | **ADSTYPE \_ CASE \_ 忽略 \_ 字串**     |
| DN                                | 1.3.6.1.4.1.1466.115.121.1.12 | **ADSTYPE \_ DN \_ 字串**               |
| DSAQualitySyntax                  | 1.3.6.1.4.1.1466.115.121.1.19 | **ADSTYPE \_ CASE \_ 忽略 \_ 字串**     |
| EnhancedGuide                     | 1.3.6.1.4.1.1466.115.121.1.21 | **ADSTYPE \_ CASE \_ 忽略 \_ 字串**     |
| FacsimileTelephoneNumber          | 1.3.6.1.4.1.1466.115.121.1.22 | **ADSTYPE \_ CASE \_ 忽略 \_ 字串**     |
| 傳真                               | 1.3.6.1.4.1.1466.115.121.1.23 | **ADSTYPE \_ 八位 \_ 字串**            |
| GeneralizedTime                   | 1.3.6.1.4.1.1466.115.121.1.24 | **ADSTYPE \_ UTC \_ 時間**                |
|  (只有網站伺服器的時間)  | 1.3.6.1.4.1.1466.115.121.1.24 | **ADSTYPE \_ UTC \_ 時間**                |
| 指南                             | 1.3.6.1.4.1.1466.115.121.1.25 | **ADSTYPE \_ CASE \_ 忽略 \_ 字串**     |
| IA5String                         | 1.3.6.1.4.1.1466.115.121.1.26 | **ADSTYPE \_ CASE \_ 忽略 \_ 字串**     |
| INTEGER                           | 1.3.6.1.4.1.1466.115.121.1.27 | **ADSTYPE \_ 整數**                  |
| INTEGER8 (不在 LDAP、NTDS)       | 1.2.840.113556.1.4.906        | **ADSTYPE \_ 大型 \_ 整數**           |
| JPEG                              | 1.3.6.1.4.1.1466.115.121.1.28 | **ADSTYPE \_ 八位 \_ 字串**            |
| MailPreference                    | 1.3.6.1.4.1.1466.115.121.1.32 | **ADSTYPE \_ CASE \_ 忽略 \_ 字串**     |
| NameAndOptionalUID                | 1.3.6.1.4.1.1466.115.121.1.34 | **ADSTYPE \_ CASE \_ 忽略 \_ 字串**     |
| NumericString                     | 1.3.6.1.4.1.1466.115.121.1.36 | **ADSTYPE \_ 數值 \_ 字串**          |
| ObjectClassDescription            | 1.3.6.1.4.1.1466.115.121.1.37 | **ADSTYPE \_ CASE \_ 忽略 \_ 字串**     |
| OctetString (不在 RFC) 中          | 1.3.6.1.4.1.1466.115.121.1.40 | **ADSTYPE \_ 八位 \_ 字串**            |
| OID                               | 1.3.6.1.4.1.1466.115.121.1.38 | **ADSTYPE \_ CASE \_ 忽略 \_ 字串**     |
| ORName                            | 1.2.840.113556.1.4.1221       | **ADSTYPE \_ CASE \_ 忽略 \_ 字串**     |
| OtherMailbox                      | 1.3.6.1.4.1.1466.115.121.1.39 | **ADSTYPE \_ CASE \_ 忽略 \_ 字串**     |
| PostalAddress                     | 1.3.6.1.4.1.1466.115.121.1.41 | **ADSTYPE \_ CASE \_ 忽略 \_ 字串**     |
| PresentationAddress               | 1.3.6.1.4.1.1466.115.121.1.43 | **ADSTYPE \_ CASE \_ 忽略 \_ 字串**     |
| PrintableString                   | 1.3.6.1.4.1.1466.115.121.1.44 | **ADSTYPE \_ 可列印的 \_ 字串**        |
| ObjectSecurityDescriptor          | 1.2.840.113556.1.4.907        | **ADSTYPE \_ NT \_ 安全 \_ 描述項** |
| TelephoneNumber                   | 1.3.6.1.4.1.1466.115.121.1.50 | **ADSTYPE \_ CASE \_ 忽略 \_ 字串**     |
| TeletexTerminalIdentifier         | 1.3.6.1.4.1.1466.115.121.1.51 | **ADSTYPE \_ 八位 \_ 字串**            |
| TelexNumber                       | 1.3.6.1.4.1.1466.115.121.1.52 | **ADSTYPE \_ CASE \_ 忽略 \_ 字串**     |
| UTCTime                           | 1.3.6.1.4.1.1466.115.121.1.53 | **ADSTYPE \_ UTC \_ 時間**                |



 

 

 




