---
title: HTTP 伺服器 API 版本2.0 資料類型
description: HTTP 伺服器 API 版本2.0 資料類型
ms.assetid: 13a0cac9-9e75-4350-a523-5ad9a57caad7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61a347b58a97ad89e499136c07f85e18ee2ce1bddc31b5c6d67b8f14a2348a44
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118950767"
---
# <a name="http-server-api-version-20-data-types"></a>HTTP 伺服器 API 版本2.0 資料類型

HTTP 伺服器 API 會使用 Http. h 標頭中所宣告的各種特殊用途識別碼類型，如下所示：

-   **USHORT** HTTP \_ 服務 \_ \_ 設定 TIMEOUT \_ 參數， \* PHTTP \_ SERVICE \_ CONFIG \_ TIMEOUT \_ 參數
-   **ULONGLONG** HTTP 不 \_ 透明 \_ 識別碼， \* PHTTP 不 \_ 透明 \_ 識別碼
-   **HTTP \_不透明 \_ 識別碼** HTTP \_ 要求 \_ 識別碼， \* PHTTP \_ 要求 \_ 識別碼
-   **HTTP \_不透明 \_ 識別碼** HTTP 連線 \_ \_ 識別碼， \* PHTTP \_ 連接 \_ 識別碼
-   **HTTP \_不透明 \_ 識別碼** HTTP \_ 原始連線 \_ \_ 識別碼， \* PHTTP \_ 原始 \_ 連接 \_ 識別碼
-   **USHORT** HTTP \_ 服務 \_ \_ 設定 TIMEOUT \_ 參數， \* PHTTP \_ SERVICE \_ CONFIG \_ TIMEOUT \_ 參數

應用程式不應該嘗試產生或修改屬於其中一種類型的任何識別碼。

 

 




