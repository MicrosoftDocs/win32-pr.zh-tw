---
description: 每個事件記錄檔都包含一個標頭 (，其 \_ \_ 具有固定大小的 ELF LOGFILE 標頭結構) ，後面接著 EVENTLOGRECORD 結構) 所代表 (的事件記錄數目，以及 ELF \_ EOF 記錄結構 (所代表的檔案結尾記錄) \_ 。
ms.assetid: 2b62b807-4ffd-4a8f-afe4-34e109d01856
title: 事件記錄檔格式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af4ba5c8bc0114e319107272e706801544e3effa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104513161"
---
# <a name="event-log-file-format"></a><span data-ttu-id="e855c-103">事件記錄檔格式</span><span class="sxs-lookup"><span data-stu-id="e855c-103">Event Log File Format</span></span>

<span data-ttu-id="e855c-104">每個事件記錄檔都包含一個標頭 (，其具有固定大小的 [**ELF \_ LOGFILE \_ 標頭**](/previous-versions/windows/desktop/legacy/bb309024(v=vs.85)) 結構) ，後面接著 [**EVENTLOGRECORD**](/windows/desktop/api/winnt/ns-winnt-eventlogrecord) 結構) 所代表 (的事件記錄數目，以及 [**ELF \_ EOF \_ 記錄**](/previous-versions/windows/desktop/legacy/bb309022(v=vs.85)) 結構 (所代表的檔案結尾記錄) 。</span><span class="sxs-lookup"><span data-stu-id="e855c-104">Each event log contains a header (represented by the [**ELF\_LOGFILE\_HEADER**](/previous-versions/windows/desktop/legacy/bb309024(v=vs.85)) structure) that has a fixed size, followed by a variable number of event records (represented by [**EVENTLOGRECORD**](/windows/desktop/api/winnt/ns-winnt-eventlogrecord) structures), and an end-of-file record (represented by the [**ELF\_EOF\_RECORD**](/previous-versions/windows/desktop/legacy/bb309022(v=vs.85)) structure).</span></span>

<span data-ttu-id="e855c-105">建立事件記錄檔時，會在事件記錄檔中寫入 ELF 記錄檔 **\_ \_ 標頭** 結構和 **ELF \_ EOF \_ 記錄** 結構，並在每次事件寫入記錄檔時更新。</span><span class="sxs-lookup"><span data-stu-id="e855c-105">The **ELF\_LOGFILE\_HEADER** structure and the **ELF\_EOF\_RECORD** structure are written in the event log when the event log is created and are updated each time an event is written to the log.</span></span>

<span data-ttu-id="e855c-106">當應用程式呼叫 [**ReportEvent**](/windows/desktop/api/Winbase/nf-winbase-reporteventa) 函式以將專案寫入事件記錄檔時，系統會將參數傳遞給事件記錄服務。</span><span class="sxs-lookup"><span data-stu-id="e855c-106">When an application calls the [**ReportEvent**](/windows/desktop/api/Winbase/nf-winbase-reporteventa) function to write an entry to the event log, the system passes the parameters to the event-logging service.</span></span> <span data-ttu-id="e855c-107">事件記錄服務會使用此資訊將 **EVENTLOGRECORD** 結構寫入事件記錄檔。</span><span class="sxs-lookup"><span data-stu-id="e855c-107">The event-logging service uses the information to write an **EVENTLOGRECORD** structure to the event log.</span></span> <span data-ttu-id="e855c-108">下圖說明此程序。</span><span class="sxs-lookup"><span data-stu-id="e855c-108">The following diagram illustrates this process.</span></span>

![寫入記錄檔](images/evreport.png)

<span data-ttu-id="e855c-110">事件記錄會以下列其中一種方式組織：</span><span class="sxs-lookup"><span data-stu-id="e855c-110">The event records are organized in one of the following ways:</span></span>

-   <span data-ttu-id="e855c-111">未換行。</span><span class="sxs-lookup"><span data-stu-id="e855c-111">Non-wrapping.</span></span> <span data-ttu-id="e855c-112">在事件記錄檔標頭之後，最舊的記錄會緊接在 **ELF \_ EOF \_ 記錄**) 之前新增 (的最後一筆記錄之後新增記錄。</span><span class="sxs-lookup"><span data-stu-id="e855c-112">The oldest record is immediately after the event log header and new records are added after the last record that was added (before the **ELF\_EOF\_RECORD**).</span></span> <span data-ttu-id="e855c-113">下列範例顯示非包裝方法：</span><span class="sxs-lookup"><span data-stu-id="e855c-113">The following example shows the non-wrapping method:</span></span>

    ``` syntax
    HEADER                   (ELF_LOGFILE_HEADER)
    EVENT RECORD 1           (EVENTLOGRECORD)
    EVENT RECORD 2           (EVENTLOGRECORD)
    EOF RECORD               (ELF_EOF_RECORD)
    ```

    <span data-ttu-id="e855c-114">當建立事件記錄檔或清除事件記錄檔時，可能會發生非換行。</span><span class="sxs-lookup"><span data-stu-id="e855c-114">Non-wrapping can occur when the event log is created or when the event log is cleared.</span></span> <span data-ttu-id="e855c-115">事件記錄檔會繼續保持未換行，直到達到事件記錄檔大小限制為止。</span><span class="sxs-lookup"><span data-stu-id="e855c-115">The event log continues to be non-wrapping until the event log size limit is reached.</span></span> <span data-ttu-id="e855c-116">事件記錄檔大小受限於 **MaxSize** 設定值或系統資源數量。</span><span class="sxs-lookup"><span data-stu-id="e855c-116">The event log size is limited by either the **MaxSize** configuration value or the amount of system resources.</span></span>

    <span data-ttu-id="e855c-117">當達到事件記錄檔大小限制時，可能會開始換行。</span><span class="sxs-lookup"><span data-stu-id="e855c-117">When the event log size limit is reached, it might start wrapping.</span></span> <span data-ttu-id="e855c-118">換行是由 **保留** 設定值所控制。</span><span class="sxs-lookup"><span data-stu-id="e855c-118">Wrapping is controlled by the **Retention** configuration value.</span></span> <span data-ttu-id="e855c-119">如需事件記錄檔設定值的詳細資訊，請參閱 [Eventlog 索引鍵](eventlog-key.md)。</span><span class="sxs-lookup"><span data-stu-id="e855c-119">For more information about the event log configuration values, see [Eventlog Key](eventlog-key.md).</span></span>

-   <span data-ttu-id="e855c-120">包裝。</span><span class="sxs-lookup"><span data-stu-id="e855c-120">Wrapping.</span></span> <span data-ttu-id="e855c-121">記錄會組織成圓形緩衝區。</span><span class="sxs-lookup"><span data-stu-id="e855c-121">The records are organized as a circular buffer.</span></span> <span data-ttu-id="e855c-122">新增記錄時，會取代最舊的記錄。</span><span class="sxs-lookup"><span data-stu-id="e855c-122">As new records are added, the oldest records are replaced.</span></span> <span data-ttu-id="e855c-123">最舊和最新記錄的位置將會有所不同。</span><span class="sxs-lookup"><span data-stu-id="e855c-123">The location of the oldest and newest records will vary.</span></span> <span data-ttu-id="e855c-124">下列範例顯示包裝方法。</span><span class="sxs-lookup"><span data-stu-id="e855c-124">The following example shows the wrapping method.</span></span>

    ``` syntax
    HEADER                   (ELF_LOGFILE_HEADER)
    Part of EVENT RECORD 300 (EVENTLOGRECORD)
    EVENT RECORD 301         (EVENTLOGRECORD)
    .
    .
    .
    EVENT RECORD 400         (EVENTLOGRECORD)
    EOF RECORD               (ELF_EOF_RECORD)
    Wasted space
    EVENT RECORD 102         (EVENTLOGRECORD)
    EVENT RECORD 103         (EVENTLOGRECORD)
    .
    .
    .
    EVENT RECORD 299         (EVENTLOGRECORD)
    Part of EVENT RECORD 300 (EVENTLOGRECORD)
    ```

    <span data-ttu-id="e855c-125">在此範例中，最舊的記錄已不再為1，但為102，因為已覆寫記錄1到101的空間。</span><span class="sxs-lookup"><span data-stu-id="e855c-125">In the example the oldest record is no longer 1, but is 102 because the space for records 1 to 101 was overwritten.</span></span>

    <span data-ttu-id="e855c-126">**ELF \_ EOF \_ 記錄** 和最舊的記錄之間有一些空間，因為系統會清除整數筆記錄，以釋放最新記錄的空間。</span><span class="sxs-lookup"><span data-stu-id="e855c-126">There is some space between the **ELF\_EOF\_RECORD** and the oldest record because the system will erase an integral number of records to free space for the newest record.</span></span> <span data-ttu-id="e855c-127">例如，如果最新記錄的長度為100個位元組，而兩個最舊的記錄是75位元組長，則系統會移除兩個最舊的記錄。</span><span class="sxs-lookup"><span data-stu-id="e855c-127">For example, if the newest record is 100 bytes long and the two oldest records are 75 bytes long, then the system will remove the two oldest records.</span></span> <span data-ttu-id="e855c-128">寫入新記錄時，稍後將會使用額外的50個位元組。</span><span class="sxs-lookup"><span data-stu-id="e855c-128">The extra 50 bytes will be used later when new records are written.</span></span>

    <span data-ttu-id="e855c-129">事件記錄檔具有固定的大小，而且當檔案中的記錄自動換行時，檔案結尾的記錄通常會分割成兩筆記錄。</span><span class="sxs-lookup"><span data-stu-id="e855c-129">An event log file has a fixed size and when the records in the file wrap, the record at the end of the file will typically be split into two records.</span></span> <span data-ttu-id="e855c-130">例如，如果下一次寫入的位置是從檔案結尾算起的100個位元組，且記錄的大小為300個位元組，則會在檔案結尾寫入前100個位元組，而下一個200位元組將會寫入檔案開頭的 **ELF \_ LOGFILE \_ 標頭** 之後。</span><span class="sxs-lookup"><span data-stu-id="e855c-130">For example, if the position for the next write is 100 bytes from the end of the file and the size of the record is 300 bytes, the first 100 bytes will be written at the end of the file and the next 200 bytes will be written at the beginning of the file immediately after the **ELF\_LOGFILE\_HEADER**.</span></span> <span data-ttu-id="e855c-131">如果位於檔案結尾的可用空間小於 **EVENTLOGRECORD** (0x38 bytes) 的固定部分，則所有新記錄都會寫入至檔案開頭的 **ELF \_ LOGFILE \_ 標頭** 之後。</span><span class="sxs-lookup"><span data-stu-id="e855c-131">If the available space at the end of the file is less than the fixed portion of the **EVENTLOGRECORD** (0x38 bytes), all of the new record will be written at the beginning of the file immediately after the **ELF\_LOGFILE\_HEADER**.</span></span> <span data-ttu-id="e855c-132">檔案結尾未使用的位元組將會填入模式0x00000027。</span><span class="sxs-lookup"><span data-stu-id="e855c-132">The unused bytes at the end of the file will be filled with the pattern 0x00000027.</span></span>

<span data-ttu-id="e855c-133">如需詳細資訊和程式碼範例，請參閱 [報告事件](reporting-an-event.md)。</span><span class="sxs-lookup"><span data-stu-id="e855c-133">For more information and a code example, see [Reporting an Event](reporting-an-event.md).</span></span>

 

 
