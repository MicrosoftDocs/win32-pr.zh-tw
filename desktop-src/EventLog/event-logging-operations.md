---
description: OpenEventLog、OpenBackupEventLog、RegisterEventSource、DeregisterEventSource 和 CloseEventLog 函數會開啟和關閉事件記錄控制碼。
ms.assetid: e42a66c2-2f1e-46f8-99c7-4701075c8ec3
title: 事件記錄作業
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 065acd268788de8c9674baa1fe47a3b89a719d4c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974406"
---
# <a name="event-logging-operations"></a><span data-ttu-id="247f7-103">事件記錄作業</span><span class="sxs-lookup"><span data-stu-id="247f7-103">Event Logging Operations</span></span>

<span data-ttu-id="247f7-104">[**OpenEventLog**](/windows/desktop/api/Winbase/nf-winbase-openeventloga)、 [**OpenBackupEventLog**](/windows/desktop/api/Winbase/nf-winbase-openbackupeventloga)、 [**RegisterEventSource**](/windows/desktop/api/Winbase/nf-winbase-registereventsourcea)、 [**DeregisterEventSource**](/windows/desktop/api/Winbase/nf-winbase-deregistereventsource)和 [**CloseEventLog**](/windows/desktop/api/Winbase/nf-winbase-closeeventlog)函數會開啟和關閉事件記錄控制碼。</span><span class="sxs-lookup"><span data-stu-id="247f7-104">The [**OpenEventLog**](/windows/desktop/api/Winbase/nf-winbase-openeventloga), [**OpenBackupEventLog**](/windows/desktop/api/Winbase/nf-winbase-openbackupeventloga), [**RegisterEventSource**](/windows/desktop/api/Winbase/nf-winbase-registereventsourcea), [**DeregisterEventSource**](/windows/desktop/api/Winbase/nf-winbase-deregistereventsource), and [**CloseEventLog**](/windows/desktop/api/Winbase/nf-winbase-closeeventlog) functions open and close event log handles.</span></span>

<span data-ttu-id="247f7-105">下表顯示可在開啟的事件記錄檔上執行的作業，以及每項作業的對應函式。</span><span class="sxs-lookup"><span data-stu-id="247f7-105">The following table shows the operations that can be performed on an open event log, and the corresponding function for each operation.</span></span>



| <span data-ttu-id="247f7-106">作業</span><span class="sxs-lookup"><span data-stu-id="247f7-106">Operation</span></span> | <span data-ttu-id="247f7-107">函式</span><span class="sxs-lookup"><span data-stu-id="247f7-107">Function</span></span>                                                                                                                     |
|-----------|------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="247f7-108">備份</span><span class="sxs-lookup"><span data-stu-id="247f7-108">Backup</span></span>    | [<span data-ttu-id="247f7-109">**BackupEventLog**</span><span class="sxs-lookup"><span data-stu-id="247f7-109">**BackupEventLog**</span></span>](/windows/desktop/api/Winbase/nf-winbase-backupeventloga)                                                                                     |
| <span data-ttu-id="247f7-110">清除</span><span class="sxs-lookup"><span data-stu-id="247f7-110">Clear</span></span>     | [<span data-ttu-id="247f7-111">**ClearEventLog**</span><span class="sxs-lookup"><span data-stu-id="247f7-111">**ClearEventLog**</span></span>](/windows/desktop/api/Winbase/nf-winbase-cleareventloga)                                                                                       |
| <span data-ttu-id="247f7-112">監視器</span><span class="sxs-lookup"><span data-stu-id="247f7-112">Monitor</span></span>   | [<span data-ttu-id="247f7-113">**NotifyChangeEventLog**</span><span class="sxs-lookup"><span data-stu-id="247f7-113">**NotifyChangeEventLog**</span></span>](/windows/desktop/api/Winbase/nf-winbase-notifychangeeventlog)                                                                         |
| <span data-ttu-id="247f7-114">查詢</span><span class="sxs-lookup"><span data-stu-id="247f7-114">Query</span></span>     | <span data-ttu-id="247f7-115">[**GetOldestEventLogRecord**](/windows/desktop/api/Winbase/nf-winbase-getoldesteventlogrecord)、 [ **GetNumberOfEventLogRecords**](/windows/desktop/api/Winbase/nf-winbase-getnumberofeventlogrecords)</span><span class="sxs-lookup"><span data-stu-id="247f7-115">[**GetOldestEventLogRecord**](/windows/desktop/api/Winbase/nf-winbase-getoldesteventlogrecord), [**GetNumberOfEventLogRecords**](/windows/desktop/api/Winbase/nf-winbase-getnumberofeventlogrecords)</span></span> |
| <span data-ttu-id="247f7-116">讀取</span><span class="sxs-lookup"><span data-stu-id="247f7-116">Read</span></span>      | [<span data-ttu-id="247f7-117">**ReadEventLog**</span><span class="sxs-lookup"><span data-stu-id="247f7-117">**ReadEventLog**</span></span>](/windows/desktop/api/Winbase/nf-winbase-readeventloga)                                                                                         |
| <span data-ttu-id="247f7-118">寫入</span><span class="sxs-lookup"><span data-stu-id="247f7-118">Write</span></span>     | [<span data-ttu-id="247f7-119">**ReportEvent**</span><span class="sxs-lookup"><span data-stu-id="247f7-119">**ReportEvent**</span></span>](/windows/desktop/api/Winbase/nf-winbase-reporteventa)                                                                                           |



 

<span data-ttu-id="247f7-120">[**OpenEventLog**](/windows/desktop/api/Winbase/nf-winbase-openeventloga)和 [**ReportEvent**](/windows/desktop/api/Winbase/nf-winbase-reporteventa)函式會採用選擇性的伺服器名稱做為參數，因此可以在遠端伺服器上執行作業。</span><span class="sxs-lookup"><span data-stu-id="247f7-120">The [**OpenEventLog**](/windows/desktop/api/Winbase/nf-winbase-openeventloga) and [**ReportEvent**](/windows/desktop/api/Winbase/nf-winbase-reporteventa) functions take an optional server name as a parameter so the operations can be performed on the remote server.</span></span> <span data-ttu-id="247f7-121">使用 [**OpenEventLog**](/windows/desktop/api/Winbase/nf-winbase-openeventloga) 來讀取或執行管理作業 (備份、清除、監視和查詢記錄檔) ，以及使用 [**RegisterEventSource**](/windows/desktop/api/Winbase/nf-winbase-registereventsourcea) 來寫入記錄檔。</span><span class="sxs-lookup"><span data-stu-id="247f7-121">Use [**OpenEventLog**](/windows/desktop/api/Winbase/nf-winbase-openeventloga) for reading or performing administrative operations (backup, clear, monitor, and query) on the log, and use [**RegisterEventSource**](/windows/desktop/api/Winbase/nf-winbase-registereventsourcea) for writing to the log.</span></span>

<span data-ttu-id="247f7-122">事件記錄函式的每個呼叫都是不可部分完成的作業。</span><span class="sxs-lookup"><span data-stu-id="247f7-122">Each call to an event logging function is an atomic operation.</span></span> <span data-ttu-id="247f7-123">當您從事件記錄檔讀取時，只會傳回整個事件記錄。</span><span class="sxs-lookup"><span data-stu-id="247f7-123">When you read from the event log, only whole event records are returned.</span></span> <span data-ttu-id="247f7-124">當您寫入事件記錄檔時，每個事件記錄都會以順序寫入記錄檔中的完整記錄。</span><span class="sxs-lookup"><span data-stu-id="247f7-124">When you write to the event log, each event record is guaranteed to be written sequentially as a complete record in the log.</span></span> <span data-ttu-id="247f7-125">下列清單描述事件記錄服務如何處理特殊條件：</span><span class="sxs-lookup"><span data-stu-id="247f7-125">The following list describes how the event-logging service handles special conditions:</span></span>

-   <span data-ttu-id="247f7-126">事件記錄服務會同時接收讀取作業和寫入作業：如果讀取位置是在檔案結尾，讀取作業會失敗並出現「檔案結尾」狀態 (如果寫入作業未完成) ，則會傳回新的記錄 (如果寫入作業已完成) 則會傳回新的記錄。</span><span class="sxs-lookup"><span data-stu-id="247f7-126">The event-logging service receives a read operation and a write operation at the same time: If the read position is at the end of the file, either the read operation fails with an "end-of-file" status (if the write operation has not been completed), or it returns the new record (if the write operation has been completed).</span></span>
-   <span data-ttu-id="247f7-127">事件記錄服務會在接收讀取作業之前完成清除作業：讀取作業失敗，並出現「檔案結尾」狀態。</span><span class="sxs-lookup"><span data-stu-id="247f7-127">The event-logging service completes a clear operation before receiving a read operation: The read operation fails with "end-of-file" status.</span></span>
-   <span data-ttu-id="247f7-128">事件記錄服務會在接收寫入作業之前完成明確的作業：清除作業會截斷記錄，然後寫入作業會在記錄檔的開頭加入新的記錄。</span><span class="sxs-lookup"><span data-stu-id="247f7-128">The event-logging service completes a clear operation before receiving a write operation: The clear operation truncates the log, then the write operation adds the new record at the beginning of the log.</span></span>

 

 



