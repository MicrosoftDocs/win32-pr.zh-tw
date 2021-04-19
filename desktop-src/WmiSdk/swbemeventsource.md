---
description: SWbemEventSource 物件會將事件查詢中的事件與 SWbemServices.ExecNotificationQuery 一起抓取。
ms.assetid: 7efd5e6a-4311-4d20-8b05-e9208eec098a
ms.tgt_platform: multiple
title: 'SWbemEventSource 物件 (>wbemdisp.tlb) '
ms.topic: reference
ms.date: 09/25/2020
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemEventSource
- ISWbemEventSource
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 8da55a7b6722c263fe9a3fb0af7a8db07d672e12
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106983551"
---
# <a name="swbemeventsource-object"></a><span data-ttu-id="e9ed5-103">SWbemEventSource 物件</span><span class="sxs-lookup"><span data-stu-id="e9ed5-103">SWbemEventSource object</span></span>

<span data-ttu-id="e9ed5-104">**SWbemEventSource** 物件會將事件查詢中的事件與 [**SWbemServices.ExecNotificationQuery**](swbemservices-execnotificationquery.md)一起抓取。</span><span class="sxs-lookup"><span data-stu-id="e9ed5-104">The **SWbemEventSource** object retrieves events from an event query in conjunction with [**SWbemServices.ExecNotificationQuery**](swbemservices-execnotificationquery.md).</span></span> <span data-ttu-id="e9ed5-105">如果您對 **SWbemServices.ExecNotificationQuery** 進行呼叫，以進行事件查詢，則會取得 **SWbemEventSource** 物件。</span><span class="sxs-lookup"><span data-stu-id="e9ed5-105">You get an **SWbemEventSource** object if you make a call to **SWbemServices.ExecNotificationQuery** to make an event query.</span></span> <span data-ttu-id="e9ed5-106">然後，您可以使用 [**NextEvent**](swbemeventsource-nextevent.md) 方法在到達時取出事件。</span><span class="sxs-lookup"><span data-stu-id="e9ed5-106">You can then use the [**NextEvent**](swbemeventsource-nextevent.md) method to retrieve events as they arrive.</span></span> <span data-ttu-id="e9ed5-107">VBScript [CreateObject](/previous-versions//xzysf6hc(v=vs.85)) 呼叫無法建立這個物件。</span><span class="sxs-lookup"><span data-stu-id="e9ed5-107">This object cannot be created by the VBScript [CreateObject](/previous-versions//xzysf6hc(v=vs.85)) call.</span></span>

## <a name="members"></a><span data-ttu-id="e9ed5-108">成員</span><span class="sxs-lookup"><span data-stu-id="e9ed5-108">Members</span></span>

<span data-ttu-id="e9ed5-109">**SWbemEventSource** 物件具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="e9ed5-109">The **SWbemEventSource** object has these types of members:</span></span>

-   [<span data-ttu-id="e9ed5-110">方法</span><span class="sxs-lookup"><span data-stu-id="e9ed5-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="e9ed5-111">屬性</span><span class="sxs-lookup"><span data-stu-id="e9ed5-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="e9ed5-112">方法</span><span class="sxs-lookup"><span data-stu-id="e9ed5-112">Methods</span></span>

<span data-ttu-id="e9ed5-113">**SWbemEventSource** 物件有這些方法。</span><span class="sxs-lookup"><span data-stu-id="e9ed5-113">The **SWbemEventSource** object has these methods.</span></span>



| <span data-ttu-id="e9ed5-114">方法</span><span class="sxs-lookup"><span data-stu-id="e9ed5-114">Method</span></span>                                          | <span data-ttu-id="e9ed5-115">描述</span><span class="sxs-lookup"><span data-stu-id="e9ed5-115">Description</span></span>                                                                                                                                  |
|:------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e9ed5-116">**NextEvent**</span><span class="sxs-lookup"><span data-stu-id="e9ed5-116">**NextEvent**</span></span>](swbemeventsource-nextevent.md) | <span data-ttu-id="e9ed5-117">用來將事件與 [**SWbemServices.ExecNotificationQuery**](swbemservices-execnotificationquery.md)一起取得。</span><span class="sxs-lookup"><span data-stu-id="e9ed5-117">Used to retrieve an event in conjunction with [**SWbemServices.ExecNotificationQuery**](swbemservices-execnotificationquery.md).</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="e9ed5-118">屬性</span><span class="sxs-lookup"><span data-stu-id="e9ed5-118">Properties</span></span>

<span data-ttu-id="e9ed5-119">**SWbemEventSource** 物件具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="e9ed5-119">The **SWbemEventSource** object has these properties.</span></span>



| <span data-ttu-id="e9ed5-120">屬性</span><span class="sxs-lookup"><span data-stu-id="e9ed5-120">Property</span></span>                                                    | <span data-ttu-id="e9ed5-121">存取類型</span><span class="sxs-lookup"><span data-stu-id="e9ed5-121">Access type</span></span>          | <span data-ttu-id="e9ed5-122">Description</span><span class="sxs-lookup"><span data-stu-id="e9ed5-122">Description</span></span>                                              |
|:------------------------------------------------------------|:---------------------|:---------------------------------------------------------|
| [<span data-ttu-id="e9ed5-123">**安全性\_**</span><span class="sxs-lookup"><span data-stu-id="e9ed5-123">**Security\_**</span></span>](swbemeventsource-security-.md)<br/> | <span data-ttu-id="e9ed5-124">唯讀</span><span class="sxs-lookup"><span data-stu-id="e9ed5-124">Read-only</span></span><br/> | <span data-ttu-id="e9ed5-125">用來讀取或變更安全性設定。</span><span class="sxs-lookup"><span data-stu-id="e9ed5-125">Used to read or change the security settings.</span></span><br/> |



 

## <a name="examples"></a><span data-ttu-id="e9ed5-126">範例</span><span class="sxs-lookup"><span data-stu-id="e9ed5-126">Examples</span></span>

<span data-ttu-id="e9ed5-127">此腳本會使用 **SWbemEventSource** 類別和 [**SWbemServices**](swbemservices.md) 類別的方法搭配應用程式事件的 WQL 查詢。</span><span class="sxs-lookup"><span data-stu-id="e9ed5-127">This script uses the methods of the **SWbemEventSource** class and the [**SWbemServices**](swbemservices.md) class in conjunction with a WQL query for application events.</span></span> <span data-ttu-id="e9ed5-128">如需 WMI 事件通知和查詢的詳細資訊，請參閱 [監視事件](monitoring-events.md)、 [根據事件執行腳本](running-a-script-based-on-an-event.md)，以及 [接收非同步事件通知](receiving-asynchronous-event-notifications.md)。</span><span class="sxs-lookup"><span data-stu-id="e9ed5-128">For more information about WMI event notification and queries see [Monitoring Events](monitoring-events.md), [Running a Script Based on an Event](running-a-script-based-on-an-event.md), and [Receiving Asynchronous Event Notifications](receiving-asynchronous-event-notifications.md).</span></span>


```VB
' Connect to WMI, obtaining an SWbemServices object
set svc = _
CreateObject("Wbemscripting.SWbemLocator")._
   ConnectServer(,"root\cimv2")

' Obtain an SWbemEventSource object from the 
' SWbemServices.ExecNotificationQuery method to specify the 
' event source as "Application" events in a Win32_NTLogEvent
set evtsrc = svc.ExecNotificationQuery("SELECT * " _
   & "FROM __InstanceCreationEvent " _
   & "WHERE TargetInstance ISA 'Win32_NTLogEvent'" _
   & "AND TargetInstance.Logfile ='Application'")

' Wait for an event by executing the NextEvent method on the 
' SWbemEventSource object.
while (num < 5)
    set inst = evtsrc.NextEvent(-1)
    Wscript.echo inst.TargetInstance.Logfile
    num = num + 1
wend
```



## <a name="requirements"></a><span data-ttu-id="e9ed5-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="e9ed5-129">Requirements</span></span>



| <span data-ttu-id="e9ed5-130">需求</span><span class="sxs-lookup"><span data-stu-id="e9ed5-130">Requirement</span></span> | <span data-ttu-id="e9ed5-131">值</span><span class="sxs-lookup"><span data-stu-id="e9ed5-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e9ed5-132">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e9ed5-132">Minimum supported client</span></span><br/> | <span data-ttu-id="e9ed5-133">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e9ed5-133">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="e9ed5-134">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e9ed5-134">Minimum supported server</span></span><br/> | <span data-ttu-id="e9ed5-135">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e9ed5-135">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="e9ed5-136">標頭</span><span class="sxs-lookup"><span data-stu-id="e9ed5-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="e9ed5-137"><dt>>wbemdisp.tlb。h</dt></span><span class="sxs-lookup"><span data-stu-id="e9ed5-137"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="e9ed5-138">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="e9ed5-138">Type library</span></span><br/>             | <dl> <span data-ttu-id="e9ed5-139"><dt>>wbemdisp.tlb .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="e9ed5-139"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="e9ed5-140">DLL</span><span class="sxs-lookup"><span data-stu-id="e9ed5-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e9ed5-141"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e9ed5-141"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="e9ed5-142">CLSID</span><span class="sxs-lookup"><span data-stu-id="e9ed5-142">CLSID</span></span><br/>                    | <span data-ttu-id="e9ed5-143">CLSID \_ SWbemEventSource</span><span class="sxs-lookup"><span data-stu-id="e9ed5-143">CLSID\_SWbemEventSource</span></span><br/>                                                      |
| <span data-ttu-id="e9ed5-144">IID</span><span class="sxs-lookup"><span data-stu-id="e9ed5-144">IID</span></span><br/>                      | <span data-ttu-id="e9ed5-145">IID \_ ISWbemEventSource</span><span class="sxs-lookup"><span data-stu-id="e9ed5-145">IID\_ISWbemEventSource</span></span><br/>                                                       |



## <a name="see-also"></a><span data-ttu-id="e9ed5-146">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e9ed5-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e9ed5-147">腳本 API 物件</span><span class="sxs-lookup"><span data-stu-id="e9ed5-147">Scripting API Objects</span></span>](scripting-api-objects.md)
</dt> </dl>

 

