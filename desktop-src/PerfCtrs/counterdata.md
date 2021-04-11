---
description: CounterData 資料表會針對在特定時間收集的每個計數器，各包含一個資料列。 這些資料列會有很多。
ms.assetid: 1253a9c7-b440-4ff2-b68c-c52b9b42a58b
title: CounterData
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e4604ce9886a6c4e3caa847dcf41a2d50b46d98
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103849295"
---
# <a name="counterdata"></a><span data-ttu-id="4c34f-104">CounterData</span><span class="sxs-lookup"><span data-stu-id="4c34f-104">CounterData</span></span>

<span data-ttu-id="4c34f-105">**CounterData** 資料表會針對在特定時間收集的每個計數器，各包含一個資料列。</span><span class="sxs-lookup"><span data-stu-id="4c34f-105">The **CounterData** table contains a row for each counter that is collected at a particular time.</span></span> <span data-ttu-id="4c34f-106">這些資料列會有很多。</span><span class="sxs-lookup"><span data-stu-id="4c34f-106">There will be a large number of these rows.</span></span>

<span data-ttu-id="4c34f-107">**CounterData** 資料表會定義下欄欄位：</span><span class="sxs-lookup"><span data-stu-id="4c34f-107">The **CounterData** table defines the following fields:</span></span>

-   <span data-ttu-id="4c34f-108">**GUID：** 此資料集的 GUID。</span><span class="sxs-lookup"><span data-stu-id="4c34f-108">**GUID:** GUID for this data set.</span></span> <span data-ttu-id="4c34f-109">使用此索引鍵與 [**DisplayToID**](displaytoid.md) 資料表聯結。</span><span class="sxs-lookup"><span data-stu-id="4c34f-109">Use this key to join with the [**DisplayToID**](displaytoid.md) table.</span></span>
-   <span data-ttu-id="4c34f-110">**CounterID：** 識別計數器。</span><span class="sxs-lookup"><span data-stu-id="4c34f-110">**CounterID:** Identifies the counter.</span></span> <span data-ttu-id="4c34f-111">使用此索引鍵與 [**CounterDetails**](counterdetails.md) 資料表聯結。</span><span class="sxs-lookup"><span data-stu-id="4c34f-111">Use this key to join with the [**CounterDetails**](counterdetails.md) table.</span></span>
-   <span data-ttu-id="4c34f-112">**RecordIndex：** 特定計數器識別碼和集合 GUID 的範例索引。</span><span class="sxs-lookup"><span data-stu-id="4c34f-112">**RecordIndex:** The sample index for a specific counter identifier and collection GUID.</span></span> <span data-ttu-id="4c34f-113">此記錄檔中每個後續範例的值會增加。</span><span class="sxs-lookup"><span data-stu-id="4c34f-113">The value increases for each successive sample in this log file.</span></span>
-   <span data-ttu-id="4c34f-114">**CounterDateTime：** 收集開始的時間（UTC 時間）。</span><span class="sxs-lookup"><span data-stu-id="4c34f-114">**CounterDateTime:** The time the collection was started, in UTC time.</span></span>
-   <span data-ttu-id="4c34f-115">**CounterValue：** 計數器的格式化值。</span><span class="sxs-lookup"><span data-stu-id="4c34f-115">**CounterValue:** The formatted value of the counter.</span></span> <span data-ttu-id="4c34f-116">如果計數器需要兩個樣本來計算可顯示的值，則第一筆記錄的這個值可能是零。</span><span class="sxs-lookup"><span data-stu-id="4c34f-116">This value may be zero for the first record if the counter requires two sample to compute a displayable value.</span></span>
-   <span data-ttu-id="4c34f-117">**FirstValueA：** 將此32位值與 **FirstValueB** 的值結合，以建立 [**PDH \_ RAW \_ 計數器**](/windows/desktop/api/Pdh/ns-pdh-pdh_raw_counter)的 **FirstValue** 成員。</span><span class="sxs-lookup"><span data-stu-id="4c34f-117">**FirstValueA:** Combine this 32-bit value with the value of **FirstValueB** to create the **FirstValue** member of [**PDH\_RAW\_COUNTER**](/windows/desktop/api/Pdh/ns-pdh-pdh_raw_counter).</span></span> <span data-ttu-id="4c34f-118">**FirstValueA** 包含低序位位。</span><span class="sxs-lookup"><span data-stu-id="4c34f-118">**FirstValueA** contains the low order bits.</span></span>
-   <span data-ttu-id="4c34f-119">**FirstValueB：** 將此32位值與 **FirstValueA** 的值結合，以建立 [**PDH \_ RAW \_ 計數器**](/windows/desktop/api/Pdh/ns-pdh-pdh_raw_counter)的 **FirstValue** 成員。</span><span class="sxs-lookup"><span data-stu-id="4c34f-119">**FirstValueB:** Combine this 32-bit value with the value of **FirstValueA** to create the **FirstValue** member of [**PDH\_RAW\_COUNTER**](/windows/desktop/api/Pdh/ns-pdh-pdh_raw_counter).</span></span> <span data-ttu-id="4c34f-120">**FirstValueB** 包含高序位位。</span><span class="sxs-lookup"><span data-stu-id="4c34f-120">**FirstValueB** contains the high order bits.</span></span>
-   <span data-ttu-id="4c34f-121">**SecondValueA：** 將此32位值與 **SecondValueB** 的值結合，以建立 [**PDH \_ RAW \_ 計數器**](/windows/desktop/api/Pdh/ns-pdh-pdh_raw_counter)的 **SecondValue** 成員。</span><span class="sxs-lookup"><span data-stu-id="4c34f-121">**SecondValueA:** Combine this 32-bit value with the value of **SecondValueB** to create the **SecondValue** member of [**PDH\_RAW\_COUNTER**](/windows/desktop/api/Pdh/ns-pdh-pdh_raw_counter).</span></span> <span data-ttu-id="4c34f-122">**SecondValueA** 包含低序位位。</span><span class="sxs-lookup"><span data-stu-id="4c34f-122">**SecondValueA** contains the low order bits.</span></span>
-   <span data-ttu-id="4c34f-123">**SecondValueB：** 將此32位值與 **SecondValueA** 的值結合，以建立 [**PDH \_ RAW \_ 計數器**](/windows/desktop/api/Pdh/ns-pdh-pdh_raw_counter)的 **SecondValue** 成員。</span><span class="sxs-lookup"><span data-stu-id="4c34f-123">**SecondValueB:** Combine this 32-bit value with the value of **SecondValueA** to create the **SecondValue** member of [**PDH\_RAW\_COUNTER**](/windows/desktop/api/Pdh/ns-pdh-pdh_raw_counter).</span></span> <span data-ttu-id="4c34f-124">**SecondValueB** 包含高序位位。</span><span class="sxs-lookup"><span data-stu-id="4c34f-124">**SecondValueB** contains the high order bits.</span></span>

<span data-ttu-id="4c34f-125">**GUID**、 **CounterID** 和 **RecordIndex** 欄位構成這個資料表的主鍵。</span><span class="sxs-lookup"><span data-stu-id="4c34f-125">The **GUID**, **CounterID**, and **RecordIndex** fields make up the primary key for this table.</span></span>

 

 



