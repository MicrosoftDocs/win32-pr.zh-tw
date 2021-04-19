---
description: 若要開啟記錄檔進行讀取，請呼叫 PdhOpenQuery 並指定記錄檔的路徑。
ms.assetid: 1d8f8662-df1f-4f84-8b65-c152f79cc5c6
title: 使用記錄檔
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba2032b90036f8f58c07d8c7e80e7e7ac2b2701c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106993134"
---
# <a name="working-with-log-files"></a><span data-ttu-id="28d05-103">使用記錄檔</span><span class="sxs-lookup"><span data-stu-id="28d05-103">Working with Log Files</span></span>

<span data-ttu-id="28d05-104">若要開啟記錄檔進行讀取，請呼叫 [**PdhOpenQuery**](/windows/desktop/api/Pdh/nf-pdh-pdhopenquerya) 並指定記錄檔的路徑。</span><span class="sxs-lookup"><span data-stu-id="28d05-104">To open a log file for reading, call [**PdhOpenQuery**](/windows/desktop/api/Pdh/nf-pdh-pdhopenquerya) and specify a path to the log file.</span></span> <span data-ttu-id="28d05-105">若要開啟記錄檔進行寫入，您必須呼叫 [**PdhOpenLog**](/windows/desktop/api/Pdh/nf-pdh-pdhopenloga)。</span><span class="sxs-lookup"><span data-stu-id="28d05-105">To open a log file for writing, you must call [**PdhOpenLog**](/windows/desktop/api/Pdh/nf-pdh-pdhopenloga).</span></span> <span data-ttu-id="28d05-106">若要關閉記錄檔，請根據您用來開啟記錄檔的功能，呼叫 [**PdhCloseQuery**](/windows/desktop/api/Pdh/nf-pdh-pdhclosequery) 或 [**PdhCloseLog**](/windows/desktop/api/Pdh/nf-pdh-pdhcloselog) 。</span><span class="sxs-lookup"><span data-stu-id="28d05-106">To close a log file, call either [**PdhCloseQuery**](/windows/desktop/api/Pdh/nf-pdh-pdhclosequery) or [**PdhCloseLog**](/windows/desktop/api/Pdh/nf-pdh-pdhcloselog) depending on which function you used to open the log file.</span></span>

## <a name="reading-from-a-log-file"></a><span data-ttu-id="28d05-107">從記錄檔讀取</span><span class="sxs-lookup"><span data-stu-id="28d05-107">Reading from a log file</span></span>

<span data-ttu-id="28d05-108">從記錄檔讀取效能資料與從即時來源讀取資料一樣：您可以開啟查詢、將計數器新增至查詢，以及呼叫 [**PdhCollectQueryData**](/windows/desktop/api/Pdh/nf-pdh-pdhcollectquerydata) 從記錄檔收集範例。</span><span class="sxs-lookup"><span data-stu-id="28d05-108">Reading performance data from a log file is the same as reading data from a real time source—you open a query, add counters to the query and call [**PdhCollectQueryData**](/windows/desktop/api/Pdh/nf-pdh-pdhcollectquerydata) to collect a sample from the log file.</span></span> <span data-ttu-id="28d05-109"> \_ \_ \_ 當您到達記錄檔的結尾時，PdhCollectQueryData 會傳回 PDH 沒有任何資料。</span><span class="sxs-lookup"><span data-stu-id="28d05-109">**PdhCollectQueryData** returns PDH\_NO\_MORE\_DATA when you reach the end of the log file.</span></span>

<span data-ttu-id="28d05-110">記錄檔中的每個範例都包含最初收集和寫入記錄檔時的時間戳記。</span><span class="sxs-lookup"><span data-stu-id="28d05-110">Each sample in the log file contains a time stamp for when it was originally collected and written to the log file.</span></span> <span data-ttu-id="28d05-111">若要取得記錄檔中第一個和最後一個範例的時間戳記，請呼叫 [**PdhGetDataSourceTimeRange**](/windows/desktop/api/Pdh/nf-pdh-pdhgetdatasourcetimerangea) 函式。</span><span class="sxs-lookup"><span data-stu-id="28d05-111">To retrieve the time stamp for the first and last sample in the log file, call the [**PdhGetDataSourceTimeRange**](/windows/desktop/api/Pdh/nf-pdh-pdhgetdatasourcetimerangea) function.</span></span> <span data-ttu-id="28d05-112">如果您想要限制從記錄檔讀取到特定時間範圍的範例，請參閱 [設定查詢的時間範圍](setting-a-time-range-for-a-query.md)。</span><span class="sxs-lookup"><span data-stu-id="28d05-112">If you want to limit the samples that you read from the log to a specific time range, see [Setting a Time Range for a Query](setting-a-time-range-for-a-query.md).</span></span>

<span data-ttu-id="28d05-113">如果您不知道記錄檔中有哪些效能物件和計數器，可以呼叫 [**PdhEnumObjects**](/windows/desktop/api/Pdh/nf-pdh-pdhenumobjectsa) 來判斷物件清單。</span><span class="sxs-lookup"><span data-stu-id="28d05-113">If you do not know which performance objects and counters exist in the log file, you can call [**PdhEnumObjects**](/windows/desktop/api/Pdh/nf-pdh-pdhenumobjectsa) to determine the list of objects.</span></span> <span data-ttu-id="28d05-114">指定物件時，您可以呼叫 [**PdhEnumObjectItems**](/windows/desktop/api/Pdh/nf-pdh-pdhenumobjectitemsa) 或 [**PdhExpandWildCardPath**](/windows/desktop/api/Pdh/nf-pdh-pdhexpandwildcardpatha) ，以抓取記錄檔中所包含的物件實例和計數器清單。</span><span class="sxs-lookup"><span data-stu-id="28d05-114">Given an object, you can call either [**PdhEnumObjectItems**](/windows/desktop/api/Pdh/nf-pdh-pdhenumobjectitemsa) or [**PdhExpandWildCardPath**](/windows/desktop/api/Pdh/nf-pdh-pdhexpandwildcardpatha) to retrieve a list of the object's instances and counters contained in the log file.</span></span>

<span data-ttu-id="28d05-115">如果您呼叫 [**PdhEnumObjectItems**](/windows/desktop/api/Pdh/nf-pdh-pdhenumobjectitemsa)，請使用實例和計數器清單，為每個可能的實例和計數器組合建立路徑。</span><span class="sxs-lookup"><span data-stu-id="28d05-115">If you call [**PdhEnumObjectItems**](/windows/desktop/api/Pdh/nf-pdh-pdhenumobjectitemsa), use the instance and counter lists to create a path for each possible combination of instance and counter.</span></span> <span data-ttu-id="28d05-116">當您呼叫 [**PdhAddCounter**](/windows/desktop/api/Pdh/nf-pdh-pdhaddcountera) 將計數器新增至查詢時，如果記錄檔不包含指定的組合，則函式會失敗。</span><span class="sxs-lookup"><span data-stu-id="28d05-116">When you call [**PdhAddCounter**](/windows/desktop/api/Pdh/nf-pdh-pdhaddcountera) to add the counter to the query, the function will fail if the log file does not contain the given combination.</span></span>

<span data-ttu-id="28d05-117">如果您使用 [**PdhExpandWildCardPath**](/windows/desktop/api/Pdh/nf-pdh-pdhexpandwildcardpatha)，您可以建立包含實例名稱和計數器萬用字元的路徑，例如， \\ 物件 (\*) \\ \* 。</span><span class="sxs-lookup"><span data-stu-id="28d05-117">If you use [**PdhExpandWildCardPath**](/windows/desktop/api/Pdh/nf-pdh-pdhexpandwildcardpatha), you can create a path that contains a wildcard for the instance name and counter, for example, \\object(\*)\\\*.</span></span> <span data-ttu-id="28d05-118">如果物件不包含實例，此函數會傳回 PDH \_ 無效 \_ 路徑。</span><span class="sxs-lookup"><span data-stu-id="28d05-118">The function returns PDH\_INVALID\_PATH if the object does not contain an instance.</span></span> <span data-ttu-id="28d05-119">在此情況下，請使用僅限計數器的萬用字元（例如物件）來呼叫 **PdhExpandWildCardPath** \\ \\ \* 。</span><span class="sxs-lookup"><span data-stu-id="28d05-119">In this case, call **PdhExpandWildCardPath** using a wildcard for counter only, for example, \\object\\\*.</span></span>

<span data-ttu-id="28d05-120">較新的作業系統可以讀取舊版作業系統上產生的記錄檔;不過，在 Windows Vista 和更新版本的作業系統上建立的記錄檔無法在舊版作業系統上讀取。</span><span class="sxs-lookup"><span data-stu-id="28d05-120">Newer operating systems can read log files that were generated on older operating systems; however, log files that were created on Windows Vista and later operating systems cannot be read on earlier operating systems.</span></span>

<span data-ttu-id="28d05-121">如需從記錄檔讀取資料的範例，請參閱 [從記錄檔讀取效能資料](reading-performance-data-from-a-log-file.md)。</span><span class="sxs-lookup"><span data-stu-id="28d05-121">For an example that reads data from a log file, see [Reading Performance Data from a Log File](reading-performance-data-from-a-log-file.md).</span></span>

## <a name="reading-from-multiple-log-files"></a><span data-ttu-id="28d05-122">從多個記錄檔讀取</span><span class="sxs-lookup"><span data-stu-id="28d05-122">Reading from multiple log files</span></span>

<span data-ttu-id="28d05-123">如果您需要建立從數個記錄檔讀取的查詢，請呼叫 [**PdhBindInputDataSource**](/windows/desktop/api/Pdh/nf-pdh-pdhbindinputdatasourcea) 將記錄檔系結在一起。</span><span class="sxs-lookup"><span data-stu-id="28d05-123">If you need to create a query that reads from several log files, call the [**PdhBindInputDataSource**](/windows/desktop/api/Pdh/nf-pdh-pdhbindinputdatasourcea) to bind the log files together.</span></span> <span data-ttu-id="28d05-124">然後，您必須使用以 ' H ' 結尾的 PDH 函式，例如 [**PdhOpenQueryH**](/windows/desktop/api/Pdh/nf-pdh-pdhopenqueryh)。</span><span class="sxs-lookup"><span data-stu-id="28d05-124">You then need to use PDH functions that end in 'H', for example, [**PdhOpenQueryH**](/windows/desktop/api/Pdh/nf-pdh-pdhopenqueryh).</span></span>

## <a name="writing-to-a-log-file"></a><span data-ttu-id="28d05-125">寫入至記錄檔</span><span class="sxs-lookup"><span data-stu-id="28d05-125">Writing to a log file</span></span>

<span data-ttu-id="28d05-126">寫入至記錄檔之前，請呼叫 [**PdhOpenQuery**](/windows/desktop/api/Pdh/nf-pdh-pdhopenquerya) 來建立查詢，並指定效能資料的來源，也就是即時資料或記錄檔。</span><span class="sxs-lookup"><span data-stu-id="28d05-126">Before writing to a log file, call [**PdhOpenQuery**](/windows/desktop/api/Pdh/nf-pdh-pdhopenquerya) to create a query and specify the source of the performance data, either real time data or a log file.</span></span> <span data-ttu-id="28d05-127">然後，新增您想要查詢的計數器。</span><span class="sxs-lookup"><span data-stu-id="28d05-127">Then, add the counters that you want to query.</span></span>

<span data-ttu-id="28d05-128">若要開啟目的地檔案，請呼叫 [**PdhOpenLog**](/windows/desktop/api/Pdh/nf-pdh-pdhopenloga)。</span><span class="sxs-lookup"><span data-stu-id="28d05-128">To open the destination file, call [**PdhOpenLog**](/windows/desktop/api/Pdh/nf-pdh-pdhopenloga).</span></span> <span data-ttu-id="28d05-129">當您開啟記錄檔時，請指定查詢。</span><span class="sxs-lookup"><span data-stu-id="28d05-129">Specify the query when you open the log file.</span></span> <span data-ttu-id="28d05-130">若要收集效能資料，並將其寫入記錄檔中，請呼叫 [**PdhUpdateLog**](/windows/desktop/api/Pdh/nf-pdh-pdhupdateloga)。</span><span class="sxs-lookup"><span data-stu-id="28d05-130">To collect the performance data and write it to the log file, call [**PdhUpdateLog**](/windows/desktop/api/Pdh/nf-pdh-pdhupdateloga).</span></span>

<span data-ttu-id="28d05-131">如果將計數器資料寫入至以逗號分隔的 ( .csv) 或以 tab 分隔的 ( tsv) 記錄檔和路徑包含萬用字元實例，則路徑會展開，而且只有在展開路徑時存在的實例才會包含在記錄檔中。</span><span class="sxs-lookup"><span data-stu-id="28d05-131">If the counter data is being written to comma-delimited (.csv) or tab-delimited (.tsv) log file and the path contains a wildcard instance, the path is expanded and only those instances that exist at the time the path is expanded are included in the log file.</span></span> <span data-ttu-id="28d05-132">但是，如果是 binary ( .blg) 或 SQL 記錄檔，則不會展開萬用字元，讓記錄檔包含記錄期間所建立的實例。</span><span class="sxs-lookup"><span data-stu-id="28d05-132">However, for binary (.blg) or SQL log files, the wildcard is not expanded so that the log file contains instances that are created during logging.</span></span>

<span data-ttu-id="28d05-133">如需將資料寫入記錄檔的範例，請參閱將 [效能資料寫入至記錄](writing-performance-data-to-a-log-file.md)檔。</span><span class="sxs-lookup"><span data-stu-id="28d05-133">For an example that writes data to a log file, see [Writing Performance Data to a Log File](writing-performance-data-to-a-log-file.md).</span></span>

## <a name="compressing-a-log-file"></a><span data-ttu-id="28d05-134">壓縮記錄檔</span><span class="sxs-lookup"><span data-stu-id="28d05-134">Compressing a log file</span></span>

<span data-ttu-id="28d05-135">您可以使用 [**PdhComputeCounterStatistics**](/windows/desktop/api/Pdh/nf-pdh-pdhcomputecounterstatistics) 函數來壓縮記錄檔。</span><span class="sxs-lookup"><span data-stu-id="28d05-135">You can use the [**PdhComputeCounterStatistics**](/windows/desktop/api/Pdh/nf-pdh-pdhcomputecounterstatistics) function to compress a log file.</span></span> <span data-ttu-id="28d05-136">例如，從記錄檔讀取十筆記錄、呼叫 **PdhComputeCounterStatistics** 來計算平均值，然後將 mean 值寫入輸出記錄檔。</span><span class="sxs-lookup"><span data-stu-id="28d05-136">For example, read ten records from a log file, call **PdhComputeCounterStatistics** to compute the mean value and then write the mean value to an output log file.</span></span>

<span data-ttu-id="28d05-137">下列主題提供使用記錄檔的其他資訊。</span><span class="sxs-lookup"><span data-stu-id="28d05-137">The following topic provides additional information on using a log file.</span></span>

-   [<span data-ttu-id="28d05-138">取得記錄檔的大小</span><span class="sxs-lookup"><span data-stu-id="28d05-138">Getting the Size of a Log File</span></span>](getting-the-size-of-a-log-file.md)

 

 



