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
# <a name="sql-log-file-schema"></a>SQL 記錄檔架構

> [!IMPORTANT]
> 對 ODBC SQL database 的 PDH 支援可能會在未來變更或無法使用。

應用程式可以使用 PDH Api 讀取和寫入相容 ODBC SQL 資料庫中的效能計數器資料，然後透過 SQL 查詢執行進一步的處理。 本節說明用來儲存效能計數器的 SQL 架構。 您可以使用此資訊來建立自訂的視圖和報表。 此架構包含下列三個數據表：

- [**CounterData**](counterdata.md)
- [**CounterDetails**](counterdetails.md)
- [**DisplayToID**](displaytoid.md)

> [!NOTE]
> 適用于 ODBC SQL database 的 PDH 支援只適用于支援 [大量複製 (BCP) 擴充](/sql/relational-databases/native-client-odbc-extensions-bulk-copy-functions/sql-server-driver-extensions-bulk-copy-functions)功能的 odbc sql 驅動程式。
