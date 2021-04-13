---
title: 關於 HTTP 伺服器 API
description: HTTP 伺服器 API 為開發人員提供了低層級的介面，可與 RFC 2616 中定義的 HTTP 功能伺服器端搭配使用。
ms.assetid: 74ad3a1d-cde2-4849-a412-d9d4101eaf12
keywords:
- HTTP 伺服器 API，總覽
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e00fcfe6527b77be32a849f00f62222396f42b5
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/20/2020
ms.locfileid: "104374603"
---
# <a name="about-http-server-api"></a>關於 HTTP 伺服器 API

HTTP 伺服器 API 為開發人員提供了低層級的介面，可與 [RFC 2616](https://www.ietf.org/rfc/rfc2616.txt)中定義的 HTTP 功能伺服器端搭配使用。 API 可讓應用程式接收導向至 Url 的 HTTP 要求，並傳送 HTTP 回應。 若要傳送動態回應，建議使用 ISAPI 或 ASP.NET 介面。

HTTP 伺服器 API 可讓多個應用程式並存于系統上，並共用相同的 TCP 埠 (例如，HTTP 的埠80或 HTTPS) 的埠443，以及提供 URL 命名空間的不同部分。

HTTP 伺服器 API 需要知道 C 程式設計語言，並熟悉 Windows API 程式設計。 不需要低層級 HTTP 存取的應用程式應該使用 IIS ISAPI 或適用于 HTTP 解決方案的 .NET Framework 類別。

 

 




