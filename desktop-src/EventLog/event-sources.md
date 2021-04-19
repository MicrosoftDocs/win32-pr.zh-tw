---
description: Eventlog 索引鍵中的每個記錄都包含稱為「事件來源」的子機碼。 事件來源是記錄事件的軟體名稱。
ms.assetid: bc7fdc74-be41-4d17-997c-27171ef73f0f
title: 事件來源
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab2b408b76cdbc6e93e44099fea2842f9655a963
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106981165"
---
# <a name="event-sources"></a><span data-ttu-id="c12d8-104">事件來源</span><span class="sxs-lookup"><span data-stu-id="c12d8-104">Event Sources</span></span>

<span data-ttu-id="c12d8-105">[Eventlog 索引鍵](eventlog-key.md)中的每個記錄都包含稱為「*事件來源*」的子機碼。</span><span class="sxs-lookup"><span data-stu-id="c12d8-105">Each log in the [Eventlog key](eventlog-key.md) contains subkeys called *event sources*.</span></span> <span data-ttu-id="c12d8-106">事件來源是記錄事件的軟體名稱。</span><span class="sxs-lookup"><span data-stu-id="c12d8-106">The event source is the name of the software that logs the event.</span></span> <span data-ttu-id="c12d8-107">如果應用程式很大，則通常是應用程式的名稱或應用程式的子元件名稱。</span><span class="sxs-lookup"><span data-stu-id="c12d8-107">It is often the name of the application or the name of a subcomponent of the application if the application is large.</span></span> <span data-ttu-id="c12d8-108">您最多可以將16384個事件來源新增至登錄。</span><span class="sxs-lookup"><span data-stu-id="c12d8-108">You can add a maximum of 16,384 event sources to the registry.</span></span> <span data-ttu-id="c12d8-109">**安全** 日誌僅供系統使用。</span><span class="sxs-lookup"><span data-stu-id="c12d8-109">The **Security** log is for system use only.</span></span> <span data-ttu-id="c12d8-110">設備磁碟機應該將其名稱新增至 **系統** 記錄檔。</span><span class="sxs-lookup"><span data-stu-id="c12d8-110">Device drivers should add their names to the **System** log.</span></span> <span data-ttu-id="c12d8-111">應用程式和服務應該將其名稱加入至 **應用程式** 記錄檔，或建立自訂記錄檔。</span><span class="sxs-lookup"><span data-stu-id="c12d8-111">Applications and services should add their names to the **Application** log or create a custom log.</span></span>

<span data-ttu-id="c12d8-112">事件來源的結構如下所示：</span><span class="sxs-lookup"><span data-stu-id="c12d8-112">The structure of the event sources is as follows:</span></span>

```
HKEY_LOCAL_MACHINE
   SYSTEM
      CurrentControlSet
         Services
            EventLog
               Application
                  AppName
               Security
               System
                  DriverName
               CustomLog
                  AppName
```

<span data-ttu-id="c12d8-113">您無法使用已做為記錄名稱的來源名稱。</span><span class="sxs-lookup"><span data-stu-id="c12d8-113">You cannot use a source name that has already been used as a log name.</span></span> <span data-ttu-id="c12d8-114">此外，來源名稱不可以是階層式;也就是說，它們不能包含反斜線字元 ( " \\ " ) 。</span><span class="sxs-lookup"><span data-stu-id="c12d8-114">In addition, source names cannot be hierarchical; that is, they cannot contain the backslash character ("\\").</span></span>

<span data-ttu-id="c12d8-115">每個事件來源都包含 (的資訊，例如會記錄事件的軟體) 特定的 [訊息](message-files.md) ，如下表所示。</span><span class="sxs-lookup"><span data-stu-id="c12d8-115">Each event source contains information (such as a [message file](message-files.md)) specific to the software that will be logging the events, as shown in the following table.</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="c12d8-116">登錄值</span><span class="sxs-lookup"><span data-stu-id="c12d8-116">Registry Value</span></span></th>
<th><span data-ttu-id="c12d8-117">Description</span><span class="sxs-lookup"><span data-stu-id="c12d8-117">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c12d8-118"><strong>CategoryCount</strong></span><span class="sxs-lookup"><span data-stu-id="c12d8-118"><strong>CategoryCount</strong></span></span></td>
<td><span data-ttu-id="c12d8-119">支援的事件類別目錄數目。</span><span class="sxs-lookup"><span data-stu-id="c12d8-119">Number of event categories supported.</span></span> <span data-ttu-id="c12d8-120">此值的類型為 <strong>REG_DWORD</strong>。</span><span class="sxs-lookup"><span data-stu-id="c12d8-120">This value is of type <strong>REG_DWORD</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c12d8-121"><strong>CategoryMessageFile</strong></span><span class="sxs-lookup"><span data-stu-id="c12d8-121"><strong>CategoryMessageFile</strong></span></span></td>
<td><span data-ttu-id="c12d8-122">類別目錄訊息檔案的路徑。</span><span class="sxs-lookup"><span data-stu-id="c12d8-122">Path to the category message file.</span></span> <span data-ttu-id="c12d8-123">類別訊息檔案包含描述分類的語言相依字串。</span><span class="sxs-lookup"><span data-stu-id="c12d8-123">A category message file contains language-dependent strings that describe the categories.</span></span> <span data-ttu-id="c12d8-124">這個值可以是類型 <strong>REG_SZ</strong> 或 <strong>REG_EXPAND_SZ</strong>。</span><span class="sxs-lookup"><span data-stu-id="c12d8-124">This value can be of type <strong>REG_SZ</strong> or <strong>REG_EXPAND_SZ</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c12d8-125"><strong>EventMessageFile</strong></span><span class="sxs-lookup"><span data-stu-id="c12d8-125"><strong>EventMessageFile</strong></span></span></td>
<td><span data-ttu-id="c12d8-126">一或多個事件訊息檔案的路徑;使用分號來分隔多個檔案。</span><span class="sxs-lookup"><span data-stu-id="c12d8-126">Path to one or more event message files; use a semicolon to delimit multiple files.</span></span> <span data-ttu-id="c12d8-127">事件訊息檔包含描述事件的語言相依字串。</span><span class="sxs-lookup"><span data-stu-id="c12d8-127">An event message file contains language-dependent strings that describe the events.</span></span> <span data-ttu-id="c12d8-128">這個值可以是類型 <strong>REG_SZ</strong> 或 <strong>REG_EXPAND_SZ</strong>。</span><span class="sxs-lookup"><span data-stu-id="c12d8-128">This value can be of type <strong>REG_SZ</strong> or <strong>REG_EXPAND_SZ</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c12d8-129"><strong>ParameterMessageFile</strong></span><span class="sxs-lookup"><span data-stu-id="c12d8-129"><strong>ParameterMessageFile</strong></span></span></td>
<td><span data-ttu-id="c12d8-130">參數訊息檔案的路徑。</span><span class="sxs-lookup"><span data-stu-id="c12d8-130">Path to the parameter message file.</span></span> <span data-ttu-id="c12d8-131">參數訊息檔案包含要插入事件描述字串的語言獨立字串。</span><span class="sxs-lookup"><span data-stu-id="c12d8-131">A parameter message file contains language-independent strings that are to be inserted into the event description strings.</span></span> <span data-ttu-id="c12d8-132">這個值可以是類型 <strong>REG_SZ</strong> 或 <strong>REG_EXPAND_SZ</strong>。</span><span class="sxs-lookup"><span data-stu-id="c12d8-132">This value can be of type <strong>REG_SZ</strong> or <strong>REG_EXPAND_SZ</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c12d8-133"><strong>TypesSupported</strong></span><span class="sxs-lookup"><span data-stu-id="c12d8-133"><strong>TypesSupported</strong></span></span></td>
<td><span data-ttu-id="c12d8-134">支援類型的位元遮罩。</span><span class="sxs-lookup"><span data-stu-id="c12d8-134">Bitmask of supported types.</span></span> <span data-ttu-id="c12d8-135">此值的類型為 <strong>REG_DWORD</strong>。</span><span class="sxs-lookup"><span data-stu-id="c12d8-135">This value is of type <strong>REG_DWORD</strong>.</span></span> <span data-ttu-id="c12d8-136">它可以是下列其中一個或多個值：</span><span class="sxs-lookup"><span data-stu-id="c12d8-136">It can be one or more of the following values:</span></span> <dl> <span data-ttu-id="c12d8-137"><strong>EVENTLOG_AUDIT_FAILURE</strong> (0x0010) </span><span class="sxs-lookup"><span data-stu-id="c12d8-137"><strong>EVENTLOG_AUDIT_FAILURE</strong> (0x0010)</span></span><br /><span data-ttu-id="c12d8-138">
<strong>EVENTLOG_AUDIT_SUCCESS</strong> (0x0008) </span><span class="sxs-lookup"><span data-stu-id="c12d8-138">
<strong>EVENTLOG_AUDIT_SUCCESS</strong> (0x0008)</span></span><br /><span data-ttu-id="c12d8-139">
<strong>EVENTLOG_ERROR_TYPE</strong> (0x0001) </span><span class="sxs-lookup"><span data-stu-id="c12d8-139">
<strong>EVENTLOG_ERROR_TYPE</strong> (0x0001)</span></span><br /><span data-ttu-id="c12d8-140">
<strong>EVENTLOG_INFORMATION_TYPE</strong> (0x0004) </span><span class="sxs-lookup"><span data-stu-id="c12d8-140">
<strong>EVENTLOG_INFORMATION_TYPE</strong> (0x0004)</span></span><br /><span data-ttu-id="c12d8-141">
<strong>EVENTLOG_WARNING_TYPE</strong> (0x0002) </span><span class="sxs-lookup"><span data-stu-id="c12d8-141">
<strong>EVENTLOG_WARNING_TYPE</strong> (0x0002)</span></span><br />
</dl></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="c12d8-142">當應用程式使用 [**RegisterEventSource**](/windows/desktop/api/Winbase/nf-winbase-registereventsourcea) 或 [**OpenEventLog**](/windows/desktop/api/Winbase/nf-winbase-openeventloga) 函數來取得事件記錄檔的控制碼時，事件記錄服務會在登錄中搜尋指定的事件來源。</span><span class="sxs-lookup"><span data-stu-id="c12d8-142">When an application uses the [**RegisterEventSource**](/windows/desktop/api/Winbase/nf-winbase-registereventsourcea) or [**OpenEventLog**](/windows/desktop/api/Winbase/nf-winbase-openeventloga) function to get a handle to an event log, the event logging service searches for the specified event source in the registry.</span></span> <span data-ttu-id="c12d8-143">例如， **應用程式** 記錄檔可能包含 Microsoft SQL Server 和 Microsoft Excel 的事件來源。</span><span class="sxs-lookup"><span data-stu-id="c12d8-143">For example, the **Application** log might contain event sources for Microsoft SQL Server and Microsoft Excel.</span></span> <span data-ttu-id="c12d8-144">如果應用程式使用 [**RegisterEventSource**](/windows/desktop/api/Winbase/nf-winbase-registereventsourcea) 或 **OpenEventLog** 搭配 Application、SQL 或 Excel 的來源名稱，事件記錄服務會將控制碼傳回給 **應用程式** 記錄檔。</span><span class="sxs-lookup"><span data-stu-id="c12d8-144">If an application uses [**RegisterEventSource**](/windows/desktop/api/Winbase/nf-winbase-registereventsourcea) or **OpenEventLog** with a source name of Application, SQL, or Excel, the event logging service returns a handle to the **Application** log.</span></span>

<span data-ttu-id="c12d8-145">應用程式可以使用 **應用程式** 記錄，而不需要將新的事件來源新增至登錄。</span><span class="sxs-lookup"><span data-stu-id="c12d8-145">An application can use the **Application** log without adding a new event source to the registry.</span></span> <span data-ttu-id="c12d8-146">如果應用程式呼叫 [**RegisterEventSource**](/windows/desktop/api/Winbase/nf-winbase-registereventsourcea) 並傳遞在登錄中找不到的來源名稱，則事件記錄服務預設會使用 **應用程式** 記錄檔。</span><span class="sxs-lookup"><span data-stu-id="c12d8-146">If the application calls [**RegisterEventSource**](/windows/desktop/api/Winbase/nf-winbase-registereventsourcea) and passes a source name that cannot be found in the registry, the event-logging service uses the **Application** log by default.</span></span> <span data-ttu-id="c12d8-147">不過，因為沒有任何訊息檔案，事件檢視器無法將任何事件識別碼或事件類別目錄對應至描述字串，而且將會顯示錯誤。</span><span class="sxs-lookup"><span data-stu-id="c12d8-147">However, because there are no message files, the Event Viewer cannot map any event identifiers or event categories to a description string, and will display an error.</span></span> <span data-ttu-id="c12d8-148">基於這個理由，您應該將唯一的事件來源加入至應用程式的登錄，並指定訊息檔。</span><span class="sxs-lookup"><span data-stu-id="c12d8-148">For this reason, you should add a unique event source to the registry for your application and specify a message file.</span></span>

 

 



