---
title: '物件識別碼 (AD DS) '
description: " (Oid 的物件識別碼) 是由各種發行授權單位所發出的唯一數值，可唯一識別資料元素、語法，以及分散式應用程式的其他部分。"
ms.assetid: a8f5a1c7-eda3-4430-b959-daef13c00a1b
ms.tgt_platform: multiple
keywords:
- 物件識別碼廣告
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2253a6173e06f5d7b0c136a520db3e1e5a5e798e
ms.sourcegitcommit: 8ea1a82717bd3dbb3457be0697329aa37fb13f08
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/11/2019
ms.locfileid: "106966434"
---
# <a name="object-identifiers-ad-ds"></a>物件識別碼 (AD DS) 

 (Oid 的物件識別碼) 是由各種發行授權單位所發出的唯一數值，可唯一識別資料元素、語法，以及分散式應用程式的其他部分。 在 OSI 應用程式、x.500 目錄、SNMP 和其他重要的應用程式中，都可以找到 Oid。 Oid 是以樹狀結構為基礎，在此結構中，較高的發行授權單位（例如 ISO）會將樹狀結構的分支配置給 subauthority，進而可以配置 subbranches。

LDAP 通訊協定 (RFC 2251) 需要目錄服務來識別具有 Oid 的物件類別、屬性和語法。 這是 LDAP X. 500 舊版的一部分。

Active Directory Domain Services 中的 Oid 包括由 ISO 針對 X. 500 類別和屬性簽發的部分，以及由 Microsoft 和其他發行授權單位所發行的部分。 OID 標記法是數位的點字串，例如 "1.2.840.113556.1.5.9"，如下表所述。



| 值  | 意義          | 描述                                              |
|--------|------------------|----------------------------------------------------------|
| 1      | ISO              | 識別根授權單位。                           |
| 2      | ANSI             | 由 ISO 指派的群組指定。                       |
| 840    | USA              | 群組指派的國家/地區指定。        |
| 113556 | Microsoft        | 國家/地區指派的組織指定。 |
| 1      | Active Directory | 由組織指派。                            |
| 5      | 類別          | 由組織指派。                            |
| 9      | **使用者** 類別   | 由組織指派。                            |



 

如需詳細資訊，以及用來取得有效 Oid 以用於擴充 Active Directory 架構的兩個程式的討論，請參閱 [取得物件識別碼](obtaining-an-object-identifier.md)。

 

 




