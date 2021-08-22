---
title: ms DS-允許對等身分的其他身分識別屬性
description: 這個屬性是用來進行存取檢查，以判斷要求者是否有許可權可以代表其他身分識別，來執行以此帳戶身分執行的服務。
ms.assetid: 38203665-4505-461b-b6ab-b634725ac2fa
ms.tgt_platform: multiple
keywords:
- ms DS-允許對等身分的其他身分識別屬性 AD 架構
- '>msds-allowedtoactonbehalfofotheridentity 屬性 AD 架構'
topic_type:
- apiref
api_name:
- ms-DS-Allowed-To-Act-On-Behalf-Of-Other-Identity
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cad3ea9795dd89777d390235193ff2663e5b514125cdf539c34dfc85ad1664bc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119552838"
---
# <a name="ms-ds-allowed-to-act-on-behalf-of-other-identity-attribute"></a>ms DS-允許對等身分的其他身分識別屬性

這個屬性是用來進行存取檢查，以判斷要求者是否有許可權可以代表其他身分識別，來執行以此帳戶身分執行的服務。



| 進入 | 值 |
|-------------------|-----------------------------------------------------|
| CN                | 以 ms DS 允許的身分識別，其他身分識別    |
| Ldap-顯示名稱 | >msds-allowedtoactonbehalfofotheridentity            |
| 大小              | \-                                                  |
| 更新許可權  | \-                                                  |
| 更新頻率  | \-                                                  |
| Attribute-Id      | 1.2.840.113556.1.4.2182                             |
| 系統識別碼-Guid    | 3f78c3e5-f79a-46bd-a0b8-9d18116ddc79                |
| Syntax            | [**String(NT-Sec-Desc)**](s-string-nt-sec-desc.md) |



## <a name="implementations"></a>實作

-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-server-2012"></a>Windows Server 2012



| 進入 | 值 |
|------------------------|--------------------------------------------------------------------|
| 連結識別碼                | \-                                                                 |
| MAPI-Id                | \-                                                                 |
| System-Only            | 是                                                               |
| 是-單一值       | 是                                                               |
| 已編制索引             | 否                                                              |
| 在通用類別目錄中      | 否                                                              |
| NT-Security-描述元 | O:BAG：不正確： S：                                                       |
| Range-Lower            | 0                                                                  |
| Range-Upper            | 132096                                                             |
| Search-Flags           | 0x00000000                                                         |
| System-Flags           | 0x00000010                                                         |
| 中使用的類別        | [**Organizational-Person**](c-organizationalperson.md)<br/> |



 

 





