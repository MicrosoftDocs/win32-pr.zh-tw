---
title: ms-DS-輸入-宣告-轉換-原則屬性
description: 這是輸入宣告的宣告轉換原則物件的連結， (宣告從受信任的網域輸入此樹系) 。
ms.assetid: 67f87782-85ed-41bb-a60d-f6c11fcda80e
ms.tgt_platform: multiple
keywords:
- ms DS-輸入-宣告-轉換-原則屬性 AD 架構
- IngressClaimsTransformationPolicy 屬性 AD 架構
topic_type:
- apiref
api_name:
- ms-DS-Ingress-Claims-Transformation-Policy
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 52d631e2f342302f8089a43a329ac3982cf7874b46ab0f60d3e4399855f573e0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118960747"
---
# <a name="ms-ds-ingress-claims-transformation-policy-attribute"></a>ms-DS-輸入-宣告-轉換-原則屬性

這是輸入宣告的宣告轉換原則物件的連結， (宣告從受信任的網域輸入此樹系) 。 這僅適用于傳出或雙向跨樹系信任。 如果不存在此連結，則會捨棄所有輸入宣告。



| 進入 | 值 |
|-------------------|--------------------------------------------|
| CN                | ms-DS-輸入-宣告-轉換-原則 |
| Ldap-顯示名稱 | IngressClaimsTransformationPolicy     |
| 大小              | \-                                         |
| 更新許可權  | \-                                         |
| 更新頻率  | \-                                         |
| Attribute-Id      | 1.2.840.113556.1.4.2191                    |
| 系統識別碼-Guid    | 86284c08-0c6e-1540-8b15-75147d23d20d       |
| Syntax            | [**Object(DS-DN)**](s-object-ds-dn.md)    |



## <a name="implementations"></a>實作

-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-server-2012"></a>Windows Server 2012



| 進入 | 值 |
|------------------------|------------------------------------------------------|
| 連結識別碼                | 2190                                                 |
| MAPI-Id                | \-                                                   |
| System-Only            | 否                                                |
| 是-單一值       | 是                                                 |
| 已編制索引             | 否                                                |
| 在通用類別目錄中      | 否                                                |
| NT-Security-描述元 | O:BAG：不正確： S：                                         |
| Range-Lower            | \-                                                   |
| Range-Upper            | \-                                                   |
| Search-Flags           | 0x00000000                                           |
| System-Flags           | 0x00000010                                           |
| 中使用的類別        | [**信任網域**](c-trusteddomain.md)<br/> |



 

 





