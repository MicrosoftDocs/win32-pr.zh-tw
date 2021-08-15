---
title: HTTP 伺服器 API 版本1.0 資料類型
description: HTTP 伺服器 API 會使用 Http .h 標頭檔中宣告為64位不帶正負號的整數的各種特殊用途識別碼類型。
ms.assetid: bec1d41e-0c80-49bc-84e1-b16c409cd0f3
keywords:
- HTTP_CONNECTION_ID 類型 HTTP
- HTTP_RAW_CONNECTION_ID 類型 HTTP
- HTTP_REQUEST_ID 類型 HTTP
- HTTP_URL_CONTEXT 類型 HTTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 151ef975470ca21c6e82e5bc7bd7bd8b99a70573385375e8552b6660ce78f631
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118950797"
---
# <a name="http-server-api-version-10-data-types"></a>HTTP 伺服器 API 版本1.0 資料類型

HTTP 伺服器 API 會使用在 Http .h 標頭檔中宣告為64位不帶正負號的整數 (**ULONGLONGs**) 的各種特殊用途識別碼類型：

-   HTTP \_ 連接 \_ 識別碼
-   HTTP \_ 原始 \_ 連接 \_ 識別碼
-   HTTP \_ 要求 \_ 識別碼
-   HTTP \_ URL \_ 內容

應用程式不應該嘗試產生或修改屬於其中一種類型的任何識別碼。

 

 




