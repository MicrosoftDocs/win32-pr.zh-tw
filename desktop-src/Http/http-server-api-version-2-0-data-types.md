---
title: HTTP 伺服器 API 版本2.0 資料類型
description: HTTP 伺服器 API 版本2.0 資料類型
ms.assetid: 13a0cac9-9e75-4350-a523-5ad9a57caad7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 670099f3303682f52fdc78397dc7f229577b94d1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106999580"
---
# <a name="http-server-api-version-20-data-types"></a><span data-ttu-id="84d7a-103">HTTP 伺服器 API 版本2.0 資料類型</span><span class="sxs-lookup"><span data-stu-id="84d7a-103">HTTP Server API Version 2.0 Data Types</span></span>

<span data-ttu-id="84d7a-104">HTTP 伺服器 API 會使用 Http. h 標頭中所宣告的各種特殊用途識別碼類型，如下所示：</span><span class="sxs-lookup"><span data-stu-id="84d7a-104">The HTTP Server API uses various special purpose identifier types declared in the Http.h header as follows:</span></span>

-   <span data-ttu-id="84d7a-105">**USHORT** HTTP \_ 服務 \_ \_ 設定 TIMEOUT \_ 參數， \* PHTTP \_ SERVICE \_ CONFIG \_ TIMEOUT \_ 參數</span><span class="sxs-lookup"><span data-stu-id="84d7a-105">**USHORT** HTTP\_SERVICE\_CONFIG\_TIMEOUT\_PARAM, \*PHTTP\_SERVICE\_CONFIG\_TIMEOUT\_PARAM</span></span>
-   <span data-ttu-id="84d7a-106">**ULONGLONG** HTTP 不 \_ 透明 \_ 識別碼， \* PHTTP 不 \_ 透明 \_ 識別碼</span><span class="sxs-lookup"><span data-stu-id="84d7a-106">**ULONGLONG** HTTP\_OPAQUE\_ID, \*PHTTP\_OPAQUE\_ID</span></span>
-   <span data-ttu-id="84d7a-107">**HTTP \_不透明 \_ 識別碼** HTTP \_ 要求 \_ 識別碼， \* PHTTP \_ 要求 \_ 識別碼</span><span class="sxs-lookup"><span data-stu-id="84d7a-107">**HTTP\_OPAQUE\_ID** HTTP\_REQUEST\_ID, \*PHTTP\_REQUEST\_ID</span></span>
-   <span data-ttu-id="84d7a-108">**HTTP \_不透明 \_ 識別碼** HTTP 連線 \_ \_ 識別碼， \* PHTTP \_ 連接 \_ 識別碼</span><span class="sxs-lookup"><span data-stu-id="84d7a-108">**HTTP\_OPAQUE\_ID** HTTP\_CONNECTION\_ID, \*PHTTP\_CONNECTION\_ID</span></span>
-   <span data-ttu-id="84d7a-109">**HTTP \_不透明 \_ 識別碼** HTTP \_ 原始連線 \_ \_ 識別碼， \* PHTTP \_ 原始 \_ 連接 \_ 識別碼</span><span class="sxs-lookup"><span data-stu-id="84d7a-109">**HTTP\_OPAQUE\_ID** HTTP\_RAW\_CONNECTION\_ID, \*PHTTP\_RAW\_CONNECTION\_ID</span></span>
-   <span data-ttu-id="84d7a-110">**USHORT** HTTP \_ 服務 \_ \_ 設定 TIMEOUT \_ 參數， \* PHTTP \_ SERVICE \_ CONFIG \_ TIMEOUT \_ 參數</span><span class="sxs-lookup"><span data-stu-id="84d7a-110">**USHORT** HTTP\_SERVICE\_CONFIG\_TIMEOUT\_PARAM, \*PHTTP\_SERVICE\_CONFIG\_TIMEOUT\_PARAM</span></span>

<span data-ttu-id="84d7a-111">應用程式不應該嘗試產生或修改屬於其中一種類型的任何識別碼。</span><span class="sxs-lookup"><span data-stu-id="84d7a-111">An application should not attempt to generate or modify any identifier that belongs to one of these types.</span></span>

 

 




