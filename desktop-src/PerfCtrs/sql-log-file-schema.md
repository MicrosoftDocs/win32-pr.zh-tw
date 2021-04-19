---
description: 應用程式可以使用 PDH 從 SQL 記錄檔中解壓縮效能計數器，也可以透過 SQL 查詢直接從資料庫解壓縮格式化或原始的計數器。
ms.assetid: 89515dd9-2d65-4b19-bb7a-ef9e7d146caa
title: SQL 記錄檔架構
ms.topic: article
ms.date: 08/17/2020
ms.openlocfilehash: 33b988194a8fda4a99f713e0026aeaddb65e9c26
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106976894"
---
# <a name="sql-log-file-schema"></a><span data-ttu-id="3a4b9-103">SQL 記錄檔架構</span><span class="sxs-lookup"><span data-stu-id="3a4b9-103">SQL Log File Schema</span></span>

> [!IMPORTANT]
> <span data-ttu-id="3a4b9-104">對 ODBC SQL database 的 PDH 支援可能會在未來變更或無法使用。</span><span class="sxs-lookup"><span data-stu-id="3a4b9-104">PDH support for ODBC SQL databases may be altered or unavailable in the future.</span></span>

<span data-ttu-id="3a4b9-105">應用程式可以使用 PDH Api 讀取和寫入相容 ODBC SQL 資料庫中的效能計數器資料，然後透過 SQL 查詢執行進一步的處理。</span><span class="sxs-lookup"><span data-stu-id="3a4b9-105">Applications can use PDH APIs read and write performance counter data in compatible ODBC SQL databases and then perform further processing through SQL queries.</span></span> <span data-ttu-id="3a4b9-106">本節說明用來儲存效能計數器的 SQL 架構。</span><span class="sxs-lookup"><span data-stu-id="3a4b9-106">This section describes the SQL schema used to store performance counters.</span></span> <span data-ttu-id="3a4b9-107">您可以使用此資訊來建立自訂的視圖和報表。</span><span class="sxs-lookup"><span data-stu-id="3a4b9-107">You can use this information to create custom views and reports.</span></span> <span data-ttu-id="3a4b9-108">此架構包含下列三個數據表：</span><span class="sxs-lookup"><span data-stu-id="3a4b9-108">The schema consists of the following three tables:</span></span>

- [<span data-ttu-id="3a4b9-109">**CounterData**</span><span class="sxs-lookup"><span data-stu-id="3a4b9-109">**CounterData**</span></span>](counterdata.md)
- [<span data-ttu-id="3a4b9-110">**CounterDetails**</span><span class="sxs-lookup"><span data-stu-id="3a4b9-110">**CounterDetails**</span></span>](counterdetails.md)
- [<span data-ttu-id="3a4b9-111">**DisplayToID**</span><span class="sxs-lookup"><span data-stu-id="3a4b9-111">**DisplayToID**</span></span>](displaytoid.md)

> [!NOTE]
> <span data-ttu-id="3a4b9-112">適用于 ODBC SQL database 的 PDH 支援只適用于支援 [大量複製 (BCP) 擴充](/sql/relational-databases/native-client-odbc-extensions-bulk-copy-functions/sql-server-driver-extensions-bulk-copy-functions)功能的 odbc sql 驅動程式。</span><span class="sxs-lookup"><span data-stu-id="3a4b9-112">PDH support for ODBC SQL databases only works with ODBC SQL drivers that support [Bulk Copy (BCP) Extensions](/sql/relational-databases/native-client-odbc-extensions-bulk-copy-functions/sql-server-driver-extensions-bulk-copy-functions).</span></span>
