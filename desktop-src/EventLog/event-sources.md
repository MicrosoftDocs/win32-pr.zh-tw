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
# <a name="event-sources"></a>事件來源

[Eventlog 索引鍵](eventlog-key.md)中的每個記錄都包含稱為「*事件來源*」的子機碼。 事件來源是記錄事件的軟體名稱。 如果應用程式很大，則通常是應用程式的名稱或應用程式的子元件名稱。 您最多可以將16384個事件來源新增至登錄。 **安全** 日誌僅供系統使用。 設備磁碟機應該將其名稱新增至 **系統** 記錄檔。 應用程式和服務應該將其名稱加入至 **應用程式** 記錄檔，或建立自訂記錄檔。

事件來源的結構如下所示：

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

您無法使用已做為記錄名稱的來源名稱。 此外，來源名稱不可以是階層式;也就是說，它們不能包含反斜線字元 ( " \\ " ) 。

每個事件來源都包含 (的資訊，例如會記錄事件的軟體) 特定的 [訊息](message-files.md) ，如下表所示。



<table>
<thead>
<tr class="header">
<th>登錄值</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>CategoryCount</strong></td>
<td>支援的事件類別目錄數目。 此值的類型為 <strong>REG_DWORD</strong>。</td>
</tr>
<tr class="even">
<td><strong>CategoryMessageFile</strong></td>
<td>類別目錄訊息檔案的路徑。 類別訊息檔案包含描述分類的語言相依字串。 這個值可以是類型 <strong>REG_SZ</strong> 或 <strong>REG_EXPAND_SZ</strong>。</td>
</tr>
<tr class="odd">
<td><strong>EventMessageFile</strong></td>
<td>一或多個事件訊息檔案的路徑;使用分號來分隔多個檔案。 事件訊息檔包含描述事件的語言相依字串。 這個值可以是類型 <strong>REG_SZ</strong> 或 <strong>REG_EXPAND_SZ</strong>。</td>
</tr>
<tr class="even">
<td><strong>ParameterMessageFile</strong></td>
<td>參數訊息檔案的路徑。 參數訊息檔案包含要插入事件描述字串的語言獨立字串。 這個值可以是類型 <strong>REG_SZ</strong> 或 <strong>REG_EXPAND_SZ</strong>。</td>
</tr>
<tr class="odd">
<td><strong>TypesSupported</strong></td>
<td>支援類型的位元遮罩。 此值的類型為 <strong>REG_DWORD</strong>。 它可以是下列其中一個或多個值： <dl> <strong>EVENTLOG_AUDIT_FAILURE</strong> (0x0010) <br />
<strong>EVENTLOG_AUDIT_SUCCESS</strong> (0x0008) <br />
<strong>EVENTLOG_ERROR_TYPE</strong> (0x0001) <br />
<strong>EVENTLOG_INFORMATION_TYPE</strong> (0x0004) <br />
<strong>EVENTLOG_WARNING_TYPE</strong> (0x0002) <br />
</dl></td>
</tr>
</tbody>
</table>



 

當應用程式使用 [**RegisterEventSource**](/windows/desktop/api/Winbase/nf-winbase-registereventsourcea) 或 [**OpenEventLog**](/windows/desktop/api/Winbase/nf-winbase-openeventloga) 函數來取得事件記錄檔的控制碼時，事件記錄服務會在登錄中搜尋指定的事件來源。 例如， **應用程式** 記錄檔可能包含 Microsoft SQL Server 和 Microsoft Excel 的事件來源。 如果應用程式使用 [**RegisterEventSource**](/windows/desktop/api/Winbase/nf-winbase-registereventsourcea) 或 **OpenEventLog** 搭配 Application、SQL 或 Excel 的來源名稱，事件記錄服務會將控制碼傳回給 **應用程式** 記錄檔。

應用程式可以使用 **應用程式** 記錄，而不需要將新的事件來源新增至登錄。 如果應用程式呼叫 [**RegisterEventSource**](/windows/desktop/api/Winbase/nf-winbase-registereventsourcea) 並傳遞在登錄中找不到的來源名稱，則事件記錄服務預設會使用 **應用程式** 記錄檔。 不過，因為沒有任何訊息檔案，事件檢視器無法將任何事件識別碼或事件類別目錄對應至描述字串，而且將會顯示錯誤。 基於這個理由，您應該將唯一的事件來源加入至應用程式的登錄，並指定訊息檔。

 

 



