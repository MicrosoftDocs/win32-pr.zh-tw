---
title: ms DS-輸出-宣告-轉換-原則屬性
description: 這是輸出宣告的宣告轉換原則物件連結， (宣告將此樹系) 至受信任的網域。
ms.assetid: 693ebb45-e90c-4629-8afc-f048c83b4b95
ms.tgt_platform: multiple
keywords:
- ms DS-輸出-宣告-轉換-原則屬性 AD 架構
- EgressClaimsTransformationPolicy 屬性 AD 架構
topic_type:
- apiref
api_name:
- ms-DS-Egress-Claims-Transformation-Policy
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f3978944b6ae85fcc5fd33682abec7dd3fff0057
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "103935424"
---
# <a name="ms-ds-egress-claims-transformation-policy-attribute"></a>ms DS-輸出-宣告-轉換-原則屬性

這是輸出宣告的宣告轉換原則物件連結， (宣告將此樹系) 至受信任的網域。 這僅適用于傳入或雙向跨樹系信任。 當此連結不存在時，所有宣告都可依現狀允許輸出。



| 進入 | 值 |
|-------------------|-------------------------------------------|
| CN                | ms DS-輸出-宣告-轉換-原則 |
| Ldap-顯示名稱 | EgressClaimsTransformationPolicy     |
| 大小              | \-                                        |
| 更新許可權  | \-                                        |
| 更新頻率  | \-                                        |
| Attribute-Id      | 1.2.840.113556.1.4.2192                   |
| 系統識別碼-Guid    | c137427e-9a73-b040-9190-1b095bb43288      |
| Syntax            | [**Object(DS-DN)**](s-object-ds-dn.md)   |



## <a name="implementations"></a>實作

-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-server-2012"></a>Windows Server 2012



| 進入 | 值 |
|------------------------|------------------------------------------------------|
| 連結識別碼                | 2192                                                 |
| MAPI-Id                | \-                                                   |
| System-Only            | 否                                                |
| 是-單一值       | 對                                                 |
| 已編制索引             | 否                                                |
| 在通用類別目錄中      | 否                                                |
| NT-Security-描述元 | O:BAG：不正確： S：                                         |
| Range-Lower            | \-                                                   |
| Range-Upper            | \-                                                   |
| Search-Flags           | 0x00000000                                           |
| System-Flags           | 0x00000010                                           |
| 中使用的類別        | [**信任網域**](c-trusteddomain.md)<br/> |



 

 





