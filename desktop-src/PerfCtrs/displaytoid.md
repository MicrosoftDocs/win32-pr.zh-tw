---
description: DisplayToID 資料表將系統監視器所顯示的使用者易記字串與其他資料表中儲存的 GUID 產生關聯。
ms.assetid: 414d16f1-ab6f-45f0-9287-154810543a6d
title: DisplayToID
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b71ae8c4ebaafc80d98580a13a83e3cc7cff815
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106975104"
---
# <a name="displaytoid"></a><span data-ttu-id="ce718-103">DisplayToID</span><span class="sxs-lookup"><span data-stu-id="ce718-103">DisplayToID</span></span>

<span data-ttu-id="ce718-104">**DisplayToID** 資料表將系統監視器所顯示的使用者易記字串與其他資料表中儲存的 GUID 產生關聯。</span><span class="sxs-lookup"><span data-stu-id="ce718-104">The **DisplayToID** table relates the user-friendly string displayed by the System Monitor to the GUID stored in the other tables.</span></span>

<span data-ttu-id="ce718-105">**DisplayToID** 資料表會定義下欄欄位：</span><span class="sxs-lookup"><span data-stu-id="ce718-105">The **DisplayToID** table defines the following fields:</span></span>

-   <span data-ttu-id="ce718-106">**GUID：** 為記錄產生的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="ce718-106">**GUID:** Unique identifier generated for a log.</span></span> <span data-ttu-id="ce718-107">此欄位是此資料表的主要索引鍵。</span><span class="sxs-lookup"><span data-stu-id="ce718-107">This field is the primary key of this table.</span></span>
-   <span data-ttu-id="ce718-108">**RunID：** 保留供內部使用。</span><span class="sxs-lookup"><span data-stu-id="ce718-108">**RunID:** Reserved for internal use.</span></span>
-   <span data-ttu-id="ce718-109">**DisplayString：** 系統監視器中所顯示的記錄檔名稱。</span><span class="sxs-lookup"><span data-stu-id="ce718-109">**DisplayString:** Name of the log file as displayed in the System Monitor.</span></span>
-   <span data-ttu-id="ce718-110">**LogStartTime：** 記錄處理常式的開始時間，以 yyyy-mm-dd hh： mm： ss： nnn 格式為限。</span><span class="sxs-lookup"><span data-stu-id="ce718-110">**LogStartTime:** Time the logging process started in yyyy-mm-dd hh:mm:ss:nnn format.</span></span>
-   <span data-ttu-id="ce718-111">**LogStopTime：** 記錄進程停止的時間，以 yyyy-mm-dd hh： mm： ss： nnn 格式為限。</span><span class="sxs-lookup"><span data-stu-id="ce718-111">**LogStopTime:** Time the logging process stopped in yyyy-mm-dd hh:mm:ss:nnn format.</span></span> <span data-ttu-id="ce718-112">您可以使用此和 **LogStartTime** 欄位中的值，來區分具有相同 **DisplayString** 值的多個記錄檔。</span><span class="sxs-lookup"><span data-stu-id="ce718-112">Multiple log files with the same **DisplayString** value can be differentiated by using the value in this and the **LogStartTime** fields.</span></span> <span data-ttu-id="ce718-113">**LogStartTime** 和 **LogStopTime** 欄位中的值也可讓您快速存取總收集時間。</span><span class="sxs-lookup"><span data-stu-id="ce718-113">The values in the **LogStartTime** and **LogStopTime** fields also allows the total collection time to be accessed quickly.</span></span>
-   <span data-ttu-id="ce718-114">**NumberOfRecords：** 資料表中為每個記錄收集所儲存的樣本數。</span><span class="sxs-lookup"><span data-stu-id="ce718-114">**NumberOfRecords:** Number of samples stored in the table for each log collection.</span></span>
-   <span data-ttu-id="ce718-115">**MinutesToUTC：** 用來將 UTC 時間儲存的資料列資料轉換為當地時間的值。</span><span class="sxs-lookup"><span data-stu-id="ce718-115">**MinutesToUTC:** Value used to convert the row data stored in UTC time to local time.</span></span>
-   <span data-ttu-id="ce718-116">**TimeZoneName：** 收集資料的時區名稱。</span><span class="sxs-lookup"><span data-stu-id="ce718-116">**TimeZoneName:** Name of the time zone where the data was collected.</span></span> <span data-ttu-id="ce718-117">如果您要從您自己的時區的系統收集或 relogged 資料，此欄位將會陳述位置。</span><span class="sxs-lookup"><span data-stu-id="ce718-117">If you are collecting or have relogged data from a file collected on systems in your own time zone, this field will state the location.</span></span>

<span data-ttu-id="ce718-118">**注意**  在 Windows Vista 之前，資料收集器集會儲存在登錄位置</span><span class="sxs-lookup"><span data-stu-id="ce718-118">**Note**  Prior to Windows Vista, the data collector sets were stored in the registry at</span></span>

<span data-ttu-id="ce718-119">**HKEY \_ LOCAL \_ MACHINE \\ SYSTEM \\ CurrentControlSet \\ Services \\ SysmonLog \\ 記錄查詢**</span><span class="sxs-lookup"><span data-stu-id="ce718-119">**HKEY\_LOCAL\_MACHINE\\SYSTEM\\CurrentControlSet\\Services\\SysmonLog\\Log Queries**</span></span>

<span data-ttu-id="ce718-120">.</span><span class="sxs-lookup"><span data-stu-id="ce718-120">.</span></span> <span data-ttu-id="ce718-121">上欄欄位未對應至 registry 中的值。</span><span class="sxs-lookup"><span data-stu-id="ce718-121">The fields listed above do not correspond to the values in registry.</span></span> <span data-ttu-id="ce718-122">在 Windows Vista 中，資料收集器集合器不會儲存在登錄中。</span><span class="sxs-lookup"><span data-stu-id="ce718-122">For Windows Vista, the data collector sets are not stored in the registry.</span></span>

 

 



