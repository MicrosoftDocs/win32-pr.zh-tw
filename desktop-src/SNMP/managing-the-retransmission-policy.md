---
title: 管理重新傳輸原則
description: WinSNMP 應用程式可以要求 Microsoft WinSNMP 實行執行應用程式的重新傳輸原則。 當執行管理重新傳輸時，它會使用其資料庫中的超時時間和重試計數值。
ms.assetid: 1f1a9589-3566-4d90-ac4d-7acf69f34676
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f2e47d983f8da62ccb8ffbe9c20b35c71bfbb70
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021778"
---
# <a name="managing-the-retransmission-policy"></a>管理重新傳輸原則

WinSNMP 應用程式可以要求 Microsoft WinSNMP 實行執行應用程式的重新傳輸原則。 當執行管理重新傳輸時，它會使用其資料庫中的超時時間和重試計數值。

實值會在初始化期間，從 [**SnmpStartup**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstartup) 函式的傳回值中識別預設的重新傳輸模式。 模式可以是下列其中一個值。



| 值        | 意義                                                                      |
|--------------|------------------------------------------------------------------------------|
| SNMPAPI \_ 于  | 此實作為執行應用程式的重新傳輸原則。     |
| SNMPAPI \_ 關閉 | 執行不會執行應用程式的重新傳輸原則。 |



 

藉由呼叫 [**SnmpGetRetransmitMode**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetretransmitmode) 函式，可讓您隨時取得目前的重新傳輸模式，以取得目前的重新傳輸模式。 WinSNMP API 提供其他 [資料庫功能](winsnmp-functions.md) ，可簡化重新傳輸原則的管理。

在程式執行期間，透過執行下列其中一個步驟，WinSNMP 應用程式可以調整原則的執行：

-   藉由呼叫 [**SnmpSetRetransmitMode**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetretransmitmode) 函式，要求執行啟動或停止執行重新傳輸原則。 如需詳細資訊，請參閱 [開啟和關閉重新傳輸](turning-retransmission-on-and-off.md)。
-   修改執行的資料庫中的超時時間和重試計數值。 如需詳細資訊，請參閱 [變更重新傳輸原則](changing-the-retransmission-policy.md)。
-   呼叫 [**SnmpCancelMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcancelmsg) 函式來取消重新傳輸週期，並釋放與單一 SNMP 訊息要求相關聯的內部資料結構。 如需詳細資訊，請參閱 [取消重新傳輸](canceling-retransmission.md)。

應用程式可以執行它自己的重新傳輸原則。 在此情況下，執行可能會或可能不會以資料庫中的值為基礎。

 

 




