---
description: 應用程式可以使用 PDH 將效能計數器從 SQL 記錄中解壓縮，也可以透過 SQL 查詢，直接從資料庫將格式化或原始的計數器解壓縮。
ms.assetid: 89515dd9-2d65-4b19-bb7a-ef9e7d146caa
title: SQL記錄檔架構
ms.topic: article
ms.date: 08/17/2020
ms.openlocfilehash: a95026c478094d8e71a44c2c57e65c2fa7044b00e982ea43187244838beed2ab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119143811"
---
# <a name="sql-log-file-schema"></a>SQL記錄檔架構

> [!IMPORTANT]
> 對 ODBC SQL 資料庫的 PDH 支援可能會在未來變更或無法使用。

應用程式可以使用 PDH api 讀取和寫入相容 ODBC SQL 資料庫中的效能計數器資料，然後透過 SQL 查詢執行進一步的處理。 本節說明用來儲存效能計數器的 SQL 架構。 您可以使用此資訊來建立自訂的視圖和報表。 此架構包含下列三個數據表：

- [**CounterData**](counterdata.md)
- [**CounterDetails**](counterdetails.md)
- [**DisplayToID**](displaytoid.md)

> [!NOTE]
> 適用于 odbc SQL 資料庫的 PDH 支援只適用于支援[大量複製 (BCP) 延伸](/sql/relational-databases/native-client-odbc-extensions-bulk-copy-functions/sql-server-driver-extensions-bulk-copy-functions)模組的 odbc SQL 驅動程式。
