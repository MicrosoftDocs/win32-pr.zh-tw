---
description: WMI 會自動將 SNMP 陷阱對應至 WMI 事件。 系統會將陷阱中包含的資料放在 WMI 事件實例的對應屬性中，以供 WMI 主機電腦存取。
ms.assetid: 549f58a9-9d3b-41b9-a374-ab83877f63a7
ms.tgt_platform: multiple
title: 以 WMI 事件的形式接收 SNMP 陷阱
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da24be8ea9a4882af0b961b1d0f6f0c3d442c70c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104513000"
---
# <a name="receiving-snmp-traps-as-wmi-events"></a>以 WMI 事件的形式接收 SNMP 陷阱

WMI 會自動將 SNMP 陷阱對應至 WMI 事件。 系統會將陷阱中包含的資料放在 WMI 事件實例的對應屬性中，以供 WMI 主機電腦存取。

> [!Note]  
> 如需安裝提供者的詳細資訊，請參閱 [設定 WMI SNMP 環境](setting-up-the-wmi-snmp-environment.md)。

 

接收 SNMP 陷阱與從任何其他 WMI 提供者接收事件幾乎完全相同。 不過，SNMP 事件篩選器在註冊事件之前，有幾個要注意的唯一類別。 此外，事件提供者需要 \\ 獨佔使用 smir 命名空間。

最常見的註冊類別為 [SnmpNotification](snmpnotification.md) 和 [SnmpExtendedNotification](snmpextendednotification.md)。 使用事件通知來更新受監視 SNMP 裝置中值的取用者意圖必須註冊 SnmpExtendedNotification 事件。 SnmpNotification 事件中的資訊無法重複使用。

下表列出設定電腦以接收 SNMP 陷阱作為 WMI 事件的相關資訊。



| Task                                                                               | Description                                                                        |
|------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [在 SNMP 事件提供者之間進行選擇](choosing-between-snmp-event-providers.md) | WMI 包含兩個 SNMP 事件提供者。                                             |
| [接收 SNMP 事件](receiving-snmp-events.md)                                 | SNMP 事件提供者支援三種類型的 SNMPv1 陷阱和 SNMPv2 通知。 |



 

下列範例會設定電腦，以監視來自受控中樞的 **SnmpLinkUpNotification** 事件。


```VB
Set objLocator = CreateObject("wbemscripting.swbemlocator")
Set objServices = objLocator.ConnectServer(, "root\snmp\mngd_hub")

set objwbemEventsource = _ 
    objServices.ExecNotificationQuery _
   ("SELECT * FROM SnmpLinkUpNotification")

set objWbemObject = objwbemEventsource.NextEvent()

wscript.echo "Received " & objWbemObject.path_.class

for each prop in objWbemObject.properties_
    wscript.echo prop.name & " -- " & prop.value
next
```



 

 



