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
# <a name="receiving-snmp-traps-as-wmi-events"></a><span data-ttu-id="7c880-104">以 WMI 事件的形式接收 SNMP 陷阱</span><span class="sxs-lookup"><span data-stu-id="7c880-104">Receiving SNMP Traps as WMI Events</span></span>

<span data-ttu-id="7c880-105">WMI 會自動將 SNMP 陷阱對應至 WMI 事件。</span><span class="sxs-lookup"><span data-stu-id="7c880-105">WMI automatically maps SNMP traps to WMI events.</span></span> <span data-ttu-id="7c880-106">系統會將陷阱中包含的資料放在 WMI 事件實例的對應屬性中，以供 WMI 主機電腦存取。</span><span class="sxs-lookup"><span data-stu-id="7c880-106">The system places the data contained in the trap in the corresponding properties of a WMI event instance for access by the WMI host machine.</span></span>

> [!Note]  
> <span data-ttu-id="7c880-107">如需安裝提供者的詳細資訊，請參閱 [設定 WMI SNMP 環境](setting-up-the-wmi-snmp-environment.md)。</span><span class="sxs-lookup"><span data-stu-id="7c880-107">For more information about installing the provider, see [Setting up the WMI SNMP Environment](setting-up-the-wmi-snmp-environment.md).</span></span>

 

<span data-ttu-id="7c880-108">接收 SNMP 陷阱與從任何其他 WMI 提供者接收事件幾乎完全相同。</span><span class="sxs-lookup"><span data-stu-id="7c880-108">Receiving an SNMP trap is nearly identical to receiving events from any other WMI provider.</span></span> <span data-ttu-id="7c880-109">不過，SNMP 事件篩選器在註冊事件之前，有幾個要注意的唯一類別。</span><span class="sxs-lookup"><span data-stu-id="7c880-109">However, the SNMP event filter has several unique classes to be aware of before registering for events.</span></span> <span data-ttu-id="7c880-110">此外，事件提供者需要 \\ 獨佔使用 smir 命名空間。</span><span class="sxs-lookup"><span data-stu-id="7c880-110">Also, the event provider requires the use of the \\smir namespace exclusively.</span></span>

<span data-ttu-id="7c880-111">最常見的註冊類別為 [SnmpNotification](snmpnotification.md) 和 [SnmpExtendedNotification](snmpextendednotification.md)。</span><span class="sxs-lookup"><span data-stu-id="7c880-111">The most common classes to register with are [SnmpNotification](snmpnotification.md) and [SnmpExtendedNotification](snmpextendednotification.md).</span></span> <span data-ttu-id="7c880-112">使用事件通知來更新受監視 SNMP 裝置中值的取用者意圖必須註冊 SnmpExtendedNotification 事件。</span><span class="sxs-lookup"><span data-stu-id="7c880-112">Consumers intent on using event notifications to update values in monitored SNMP devices must register for SnmpExtendedNotification events.</span></span> <span data-ttu-id="7c880-113">SnmpNotification 事件中的資訊無法重複使用。</span><span class="sxs-lookup"><span data-stu-id="7c880-113">The information from SnmpNotification events is not reusable.</span></span>

<span data-ttu-id="7c880-114">下表列出設定電腦以接收 SNMP 陷阱作為 WMI 事件的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="7c880-114">The following table lists information about setting up your computer to receive SNMP traps as WMI events.</span></span>



| <span data-ttu-id="7c880-115">Task</span><span class="sxs-lookup"><span data-stu-id="7c880-115">Task</span></span>                                                                               | <span data-ttu-id="7c880-116">Description</span><span class="sxs-lookup"><span data-stu-id="7c880-116">Description</span></span>                                                                        |
|------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [<span data-ttu-id="7c880-117">在 SNMP 事件提供者之間進行選擇</span><span class="sxs-lookup"><span data-stu-id="7c880-117">Choosing Between SNMP Event Providers</span></span>](choosing-between-snmp-event-providers.md) | <span data-ttu-id="7c880-118">WMI 包含兩個 SNMP 事件提供者。</span><span class="sxs-lookup"><span data-stu-id="7c880-118">WMI includes two SNMP event providers.</span></span>                                             |
| [<span data-ttu-id="7c880-119">接收 SNMP 事件</span><span class="sxs-lookup"><span data-stu-id="7c880-119">Receiving SNMP Events</span></span>](receiving-snmp-events.md)                                 | <span data-ttu-id="7c880-120">SNMP 事件提供者支援三種類型的 SNMPv1 陷阱和 SNMPv2 通知。</span><span class="sxs-lookup"><span data-stu-id="7c880-120">SNMP event providers support three types of SNMPv1 traps and SNMPv2 notifications.</span></span> |



 

<span data-ttu-id="7c880-121">下列範例會設定電腦，以監視來自受控中樞的 **SnmpLinkUpNotification** 事件。</span><span class="sxs-lookup"><span data-stu-id="7c880-121">The following example sets up a computer to monitor for the **SnmpLinkUpNotification** event from a managed hub.</span></span>


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



 

 



