---
description: 時間相關函數會以數種格式的其中一種傳回時間。 您可以使用時間函數在某些時間格式之間進行轉換，以方便比較和顯示。 下表摘要說明時間格式。
ms.assetid: 74feb158-ba45-4660-970b-3eb577b1ebf8
title: 是時候了
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02a95571637bb480920f82e90011a72f6eba9e8a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104026866"
---
# <a name="about-time"></a><span data-ttu-id="7cd09-105">是時候了</span><span class="sxs-lookup"><span data-stu-id="7cd09-105">About Time</span></span>

<span data-ttu-id="7cd09-106">時間相關函數會以數種格式的其中一種傳回時間。</span><span class="sxs-lookup"><span data-stu-id="7cd09-106">Time-related functions return time in one of several formats.</span></span> <span data-ttu-id="7cd09-107">您可以使用時間函數在某些時間格式之間進行轉換，以方便比較和顯示。</span><span class="sxs-lookup"><span data-stu-id="7cd09-107">You can use the time functions to convert between some time formats for ease of comparison and display.</span></span> <span data-ttu-id="7cd09-108">下表摘要說明時間格式。</span><span class="sxs-lookup"><span data-stu-id="7cd09-108">The following table summarizes the time formats.</span></span>



| <span data-ttu-id="7cd09-109">格式</span><span class="sxs-lookup"><span data-stu-id="7cd09-109">Format</span></span>          | <span data-ttu-id="7cd09-110">類型</span><span class="sxs-lookup"><span data-stu-id="7cd09-110">Type</span></span>                                                                     | <span data-ttu-id="7cd09-111">Description</span><span class="sxs-lookup"><span data-stu-id="7cd09-111">Description</span></span>                                                                                                                         |
|-----------------|--------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7cd09-112">系統</span><span class="sxs-lookup"><span data-stu-id="7cd09-112">System</span></span>          | [<span data-ttu-id="7cd09-113">**SYSTEMTIME**</span><span class="sxs-lookup"><span data-stu-id="7cd09-113">**SYSTEMTIME**</span></span>](/windows/win32/api/minwinbase/ns-minwinbase-systemtime)                                     | <span data-ttu-id="7cd09-114">取自內部硬體時鐘的年、月、日、小時、秒和毫秒。</span><span class="sxs-lookup"><span data-stu-id="7cd09-114">Year, month, day, hour, second, and millisecond, taken from the internal hardware clock.</span></span>                                            |
| <span data-ttu-id="7cd09-115">本機</span><span class="sxs-lookup"><span data-stu-id="7cd09-115">Local</span></span>           | <span data-ttu-id="7cd09-116">[**SYSTEMTIME**](/windows/win32/api/minwinbase/ns-minwinbase-systemtime)或 [ **FILETIME**](/windows/win32/api/minwinbase/ns-minwinbase-filetime)</span><span class="sxs-lookup"><span data-stu-id="7cd09-116">[**SYSTEMTIME**](/windows/win32/api/minwinbase/ns-minwinbase-systemtime) or [**FILETIME**](/windows/win32/api/minwinbase/ns-minwinbase-filetime)</span></span> | <span data-ttu-id="7cd09-117">轉換成系統本地時區的系統時間或檔案時間。</span><span class="sxs-lookup"><span data-stu-id="7cd09-117">A system time or file time converted to the system's local time zone.</span></span>                                                               |
| <span data-ttu-id="7cd09-118">檔案</span><span class="sxs-lookup"><span data-stu-id="7cd09-118">File</span></span>            | [<span data-ttu-id="7cd09-119">**FILETIME**</span><span class="sxs-lookup"><span data-stu-id="7cd09-119">**FILETIME**</span></span>](/windows/win32/api/minwinbase/ns-minwinbase-filetime)                                         | <span data-ttu-id="7cd09-120">自1601年1月1日起的 100-毫微秒間隔數目。</span><span class="sxs-lookup"><span data-stu-id="7cd09-120">The number of 100-nanosecond intervals since January 1, 1601.</span></span>                                                                       |
| <span data-ttu-id="7cd09-121">MS-DOS</span><span class="sxs-lookup"><span data-stu-id="7cd09-121">MS-DOS</span></span>          | <span data-ttu-id="7cd09-122">**WORD**</span><span class="sxs-lookup"><span data-stu-id="7cd09-122">**WORD**</span></span>                                                                 | <span data-ttu-id="7cd09-123">日期的壓縮文字，另一個用於時間。</span><span class="sxs-lookup"><span data-stu-id="7cd09-123">A packed word for the date, another for the time.</span></span>                                                                                   |
| <span data-ttu-id="7cd09-124">Windows</span><span class="sxs-lookup"><span data-stu-id="7cd09-124">Windows</span></span>         | <span data-ttu-id="7cd09-125">**DWORD** 或 **ULONGLONG**</span><span class="sxs-lookup"><span data-stu-id="7cd09-125">**DWORD** or **ULONGLONG**</span></span>                                               | <span data-ttu-id="7cd09-126">自上次啟動系統之後的毫秒數。</span><span class="sxs-lookup"><span data-stu-id="7cd09-126">The number of milliseconds since the system was last started.</span></span> <span data-ttu-id="7cd09-127">以 DWORD 值形式取出時，Windows 時間會每隔49.7 天迴圈。</span><span class="sxs-lookup"><span data-stu-id="7cd09-127">When retrieved as a DWORD value, Windows time cycles every 49.7 days.</span></span> |
| <span data-ttu-id="7cd09-128">中斷計數</span><span class="sxs-lookup"><span data-stu-id="7cd09-128">Interrupt Count</span></span> | <span data-ttu-id="7cd09-129">**ULONGLONG**</span><span class="sxs-lookup"><span data-stu-id="7cd09-129">**ULONGLONG**</span></span>                                                            | <span data-ttu-id="7cd09-130">自系統上次啟動後的 100-毫微秒間隔數目。</span><span class="sxs-lookup"><span data-stu-id="7cd09-130">The number of 100-nanosecond intervals since the system was last started.</span></span>                                                           |



 

<span data-ttu-id="7cd09-131">如需詳細資訊，請參閱下列主題：</span><span class="sxs-lookup"><span data-stu-id="7cd09-131">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="7cd09-132">系統時間</span><span class="sxs-lookup"><span data-stu-id="7cd09-132">System Time</span></span>](system-time.md)
-   [<span data-ttu-id="7cd09-133">當地時間</span><span class="sxs-lookup"><span data-stu-id="7cd09-133">Local Time</span></span>](local-time.md)
-   [<span data-ttu-id="7cd09-134">檔案時間</span><span class="sxs-lookup"><span data-stu-id="7cd09-134">File Times</span></span>](file-times.md)
-   [<span data-ttu-id="7cd09-135">MS-DOS 日期和時間</span><span class="sxs-lookup"><span data-stu-id="7cd09-135">MS-DOS Date and Time</span></span>](ms-dos-date-and-time.md)
-   [<span data-ttu-id="7cd09-136">Windows Time</span><span class="sxs-lookup"><span data-stu-id="7cd09-136">Windows Time</span></span>](windows-time.md)
-   [<span data-ttu-id="7cd09-137">停機時間</span><span class="sxs-lookup"><span data-stu-id="7cd09-137">Interrupt Time</span></span>](interrupt-time.md)

 

 
