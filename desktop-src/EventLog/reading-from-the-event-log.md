---
description: 事件檢視器應用程式會使用 OpenEventLog 函數來開啟事件來源的事件記錄檔。
ms.assetid: f10ea874-66a6-446a-a18a-0c008c2da64f
title: 從事件記錄檔讀取
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4642c003d31c986be55a819b513f1c28c784af2a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104026586"
---
# <a name="reading-from-the-event-log"></a><span data-ttu-id="92424-103">從事件記錄檔讀取</span><span class="sxs-lookup"><span data-stu-id="92424-103">Reading from the Event Log</span></span>

<span data-ttu-id="92424-104">事件檢視器應用程式會使用 [**OpenEventLog**](/windows/desktop/api/Winbase/nf-winbase-openeventloga) 函數來開啟事件來源的事件記錄檔。</span><span class="sxs-lookup"><span data-stu-id="92424-104">An event viewer application uses the [**OpenEventLog**](/windows/desktop/api/Winbase/nf-winbase-openeventloga) function to open the event log for an event source.</span></span> <span data-ttu-id="92424-105">然後，事件檢視器可以使用 [**ReadEventLog**](/windows/desktop/api/Winbase/nf-winbase-readeventloga) 函式來讀取記錄檔中的事件記錄。</span><span class="sxs-lookup"><span data-stu-id="92424-105">The event viewer can then use the [**ReadEventLog**](/windows/desktop/api/Winbase/nf-winbase-readeventloga) function to read event records from the log.</span></span> <span data-ttu-id="92424-106">**ReadEventLog** 會傳回包含 [**EVENTLOGRECORD**](/windows/desktop/api/Winnt/ns-winnt-eventlogrecord) 結構的緩衝區，以及描述所記錄事件的其他資訊。</span><span class="sxs-lookup"><span data-stu-id="92424-106">**ReadEventLog** returns a buffer containing an [**EVENTLOGRECORD**](/windows/desktop/api/Winnt/ns-winnt-eventlogrecord) structure and additional information that describes a logged event.</span></span> <span data-ttu-id="92424-107">下圖說明此程序。</span><span class="sxs-lookup"><span data-stu-id="92424-107">The following diagram illustrates this process.</span></span>

![從事件記錄檔讀取](images/readlog.png)

<span data-ttu-id="92424-109">如需範例程式碼，請參閱 [查詢事件資訊](querying-for-event-source-messages.md)。</span><span class="sxs-lookup"><span data-stu-id="92424-109">For example code, see [Querying for Event Information](querying-for-event-source-messages.md).</span></span>

 

 



