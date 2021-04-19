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
ms.openlocfilehash: 681e24c06334a9010287e2084d9d6a04428ca6a1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106968666"
---
# <a name="http-server-api-version-10-data-types"></a>HTTP 伺服器 API 版本1.0 資料類型

HTTP 伺服器 API 會使用在 Http .h 標頭檔中宣告為64位不帶正負號的整數 (**ULONGLONGs**) 的各種特殊用途識別碼類型：

-   HTTP \_ 連接 \_ 識別碼
-   HTTP \_ 原始 \_ 連接 \_ 識別碼
-   HTTP \_ 要求 \_ 識別碼
-   HTTP \_ URL \_ 內容

應用程式不應該嘗試產生或修改屬於其中一種類型的任何識別碼。

 

 




