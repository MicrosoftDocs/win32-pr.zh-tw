---
title: SNMP 的運作方式
description: 協力廠商 SNMP 管理主控台應用程式如何從 SNMP 服務傳回信息。
ms.assetid: 2edbf9ff-b9e3-4103-affc-a5c0f22b80a1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1feb82b50a954ef96310b887b9fc6e73694242b639a354cd29a5c328c43daf5d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119009466"
---
# <a name="how-snmp-works"></a>SNMP 的運作方式

下列步驟概述協力廠商 SNMP 管理主控台應用程式如何從 SNMP 服務傳回信息：

1.  SNMP 管理主控台應用程式會根據使用者的輸入來會構成 SNMP 訊息。 此訊息包含通訊協定資料單位 (PDU) 和驗證資訊。 管理主控台應用程式可以使用 Microsoft SNMP 管理 API 程式庫 (MGMTAPI.DLL) 或 Microsoft [WINSNMP API](winsnmp-api.md) 程式庫 (WSNMP32.DLL) 來執行此步驟。
2.  SNMP 管理主控台應用程式會使用 SNMP 服務程式庫，將 SNMP 訊息傳送至 SNMP 服務。
3.  SNMP 服務收到要求。 它會驗證驗證資訊和來源 IP 位址。
4.  SNMP 服務會選取適當的擴充代理程式，並要求代理程式取得要求的資訊。
5.  SNMP 服務會將回應傳送至 SNMP 管理主控台應用程式。

 

 




