---
description: 如果資料來源是記錄檔，您可以指定查詢的時間範圍。
ms.assetid: 8d9c3e96-3645-4875-9b5f-a6c9ddf23ec3
title: 設定查詢的時間範圍
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55baf642a4a12a86476e2d6feada6b79f1fda72c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106969358"
---
# <a name="setting-a-time-range-for-a-query"></a><span data-ttu-id="4fedb-103">設定查詢的時間範圍</span><span class="sxs-lookup"><span data-stu-id="4fedb-103">Setting a Time Range for a Query</span></span>

<span data-ttu-id="4fedb-104">如果資料來源是記錄檔，您可以指定查詢的時間範圍。</span><span class="sxs-lookup"><span data-stu-id="4fedb-104">If the data source is a log file, you can specify a time range for the query.</span></span> <span data-ttu-id="4fedb-105">此查詢會從在指定時間範圍內收集的記錄檔中，抓取計數器資料。</span><span class="sxs-lookup"><span data-stu-id="4fedb-105">The query retrieves counter data from the log file that was collected during the specified time range.</span></span> <span data-ttu-id="4fedb-106">若要設定時間範圍，請呼叫 [**PdhSetQueryTimeRange**](/windows/desktop/api/Pdh/nf-pdh-pdhsetquerytimerange) 函數。</span><span class="sxs-lookup"><span data-stu-id="4fedb-106">To set the time range, call the [**PdhSetQueryTimeRange**](/windows/desktop/api/Pdh/nf-pdh-pdhsetquerytimerange) function.</span></span> <span data-ttu-id="4fedb-107">**PdhSetQueryTimeRange** 不會用來從即時資料源查詢效能資料。</span><span class="sxs-lookup"><span data-stu-id="4fedb-107">**PdhSetQueryTimeRange** is not used to query performance data from real time data sources.</span></span>

<span data-ttu-id="4fedb-108">若要建立時間值，請使用下列步驟。</span><span class="sxs-lookup"><span data-stu-id="4fedb-108">To create time value, use the following steps.</span></span>

1.  <span data-ttu-id="4fedb-109">配置 [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) 結構，並使用所需的時間值來初始化欄位。</span><span class="sxs-lookup"><span data-stu-id="4fedb-109">Allocate a [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) structure and initialize the fields with the desired time value.</span></span>
2.  <span data-ttu-id="4fedb-110">呼叫 [**SystemTimeToFileTime**](/windows/desktop/api/timezoneapi/nf-timezoneapi-systemtimetofiletime) 將 [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) 結構時間值轉換成 [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) 結構時間。</span><span class="sxs-lookup"><span data-stu-id="4fedb-110">Call [**SystemTimeToFileTime**](/windows/desktop/api/timezoneapi/nf-timezoneapi-systemtimetofiletime) to convert the [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) structure time value to a [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) structure time.</span></span>
3.  <span data-ttu-id="4fedb-111">將 [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) 結構轉換成 LONGLONG 變數，並記住平臺和編譯器的結構成員填補慣例。</span><span class="sxs-lookup"><span data-stu-id="4fedb-111">Cast the [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) structure as a LONGLONG variable, keeping in mind the structure member padding conventions of your platform and compiler.</span></span>
4.  <span data-ttu-id="4fedb-112">將 LONGLONG 值複製到 [**PDH \_ 時間 \_ 資訊**](/windows/desktop/api/Pdh/ns-pdh-pdh_time_info) 結構中的適當欄位。</span><span class="sxs-lookup"><span data-stu-id="4fedb-112">Copy the LONGLONG value to the appropriate field in the [**PDH\_TIME\_INFO**](/windows/desktop/api/Pdh/ns-pdh-pdh_time_info) structure.</span></span>

<span data-ttu-id="4fedb-113">若要取出記錄檔中所包含之所有效能資料的時間範圍，請呼叫 [**PdhGetDataSourceTimeRange**](/windows/desktop/api/Pdh/nf-pdh-pdhgetdatasourcetimerangea) 函式。</span><span class="sxs-lookup"><span data-stu-id="4fedb-113">To retrieve the time range of all of the performance data contained in a log file, call the [**PdhGetDataSourceTimeRange**](/windows/desktop/api/Pdh/nf-pdh-pdhgetdatasourcetimerangea) function.</span></span>

 

 
