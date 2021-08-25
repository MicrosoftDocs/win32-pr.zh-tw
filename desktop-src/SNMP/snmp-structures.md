---
title: SNMP 結構
description: 下表列出與 SNMP 搭配使用的結構。
ms.assetid: b6dacc85-893d-4825-93df-729333b491b3
keywords:
- SNMP 結構 SNMP
- 結構 SNMP，SNMP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bb5cf0920d9387fb24874cc92a8e7fa623617d89f3578cb181805eb56f35546
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119886348"
---
# <a name="snmp-structures"></a>SNMP 結構

\[SNMP 可用於 [需求] 區段中指定的作業系統。 它在後續版本中可能會變更或無法使用。 相反地，請使用[Windows 遠端管理](/windows/desktop/WinRM/portal)，也就是 Microsoft 對 ws-atomictransaction 的實。\]

下表列出與 SNMP 搭配使用的結構。



| SNMP 結構                                         | 描述                                                                                             |
|--------------------------------------------------------|---------------------------------------------------------------------------------------------------------|
| [**AsnAny**](/windows/desktop/api/Snmp/ns-snmp-asnany)                           | 描述指定之 SNMP 變數的類型和值。                                              |
| [**AsnCounter64**](/previous-versions/windows/desktop/legacy/aa377953(v=vs.85))               | 包含64位的計數器，此計數器是由描述其低序位和高序位位的兩個值所指定。 |
| [**AsnObjectIdentifier**](/windows/desktop/api/Snmp/ns-snmp-asnobjectidentifier) | 描述 (OID) 的物件識別碼。                                                                   |
| [**AsnOctetString**](/windows/desktop/api/Snmp/ns-snmp-asnoctetstring)           | 代表八位元組的字串，通常是位元組值。                                                  |
| [**SnmpVarBind**](/windows/desktop/api/Snmp/ns-snmp-snmpvarbind)                 | 描述 SNMP 變數系結。                                                                     |
| [**SnmpVarBindList**](/windows/desktop/api/Snmp/ns-snmp-snmpvarbindlist)         | 包含 SNMP 變數系結的清單。                                                              |



 

 

 