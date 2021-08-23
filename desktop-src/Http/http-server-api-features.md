---
title: HTTP 伺服器 API 功能
description: 本主題支援和不支援的 HTTP 伺服器 API 功能。
ms.assetid: 448fe5a5-e79f-4c3a-aa76-94cff988f24f
keywords:
- HTTP 伺服器 API 功能
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0eaf567d4576618b07ef5ad8dec91b360f37ab46eb820ff52e2bca896ca91a36
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119014776"
---
# <a name="http-server-api-features"></a>HTTP 伺服器 API 功能

下列清單描述 HTTP 伺服器 API 支援和不支援的功能。

## <a name="features-supported"></a>支援的功能

HTTP 支援下列功能：

-   HTTP v1.0 和 v1.1 伺服器功能。
-   安全通訊端層 3.0 (SSL) 支援用戶端和伺服器憑證。
-   要在後續回應中使用的資料片段快取。
-   支援 IPv6 和 IPv4 定址。
-   應用程式安全性的 URL 命名空間保留專案。
-   所有物件的真正控制碼。
-   同步和非同步 i/o 模型。
-   在64位上執行的電腦上支援 WOW64 Windows 從 Windows Server 2003 Service Pack 1 (SP1) 開始。

## <a name="features-not-supported"></a>不支援的功能

HTTP 伺服器 API 不支援下列功能：

-   HTTP 伺服器 API 不會根據 HTTP 要求標頭的內容執行用戶端或伺服器驗證。 應用程式必須執行任何必要的驗證。
-   Windows Server 2003 和 Windows XP Service Pack 2 (SP2) 及更早版本中，不支援在執行64位 Windows 電腦上的 WOW64。
-   HTTP 伺服器 API 不支援記錄 HTTP 要求和回應。
-   HTTP 伺服器 API 不會將傳出的 HTTP 回應區塊。 如果需要，應用程式必須執行回應區塊化。

 

 




