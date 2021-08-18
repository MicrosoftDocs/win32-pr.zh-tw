---
title: 管理變數系結清單
description: SnmpGetVb 函式會從變數系結清單中捕獲變數系結資訊。 函數會從 WinSNMP 應用程式所指定的變數系結專案中，抓取變數名稱和變數的相關聯值。
ms.assetid: 357aebd6-171a-4221-b12a-712702f9d9c6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9c382e2780ae49a1f029aab2cfef2bcd4357fcfbf7b37ce9a1fcad9aed5bc0e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119009446"
---
# <a name="managing-a-variable-binding-list"></a>管理變數系結清單

[**SnmpGetVb**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetvb)函式會從變數系結清單中捕獲變數系結資訊。 函數會從 WinSNMP 應用程式所指定的變數系結專案中，抓取變數名稱和變數的相關聯值。

若要更新變數系結清單中的變數繫結項目，請呼叫 [**SnmpSetVb**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetvb) 函數。 **SnmpSetVb** 函式也會將新的變數繫結項目附加至現有的變數系結清單。

WinSNMP 應用程式必須呼叫 [**SnmpDeleteVb**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpdeletevb) 函式，才能從變數系結清單中移除專案。

若要抓取、修改或刪除變數系結專案，WinSNMP 應用程式必須在變數系結清單中指定專案的位置。

[**SnmpSetPduData**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetpdudata)函式的呼叫會將變數系結清單與 PDU 產生關聯。 [**SnmpGetPduData**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetpdudata)函式的呼叫會從 PDU 取出變數系結清單。 個別的變數系結不會直接與 PDU 相關聯，但會透過其包含在變數系結清單中間接關聯。

 

 




