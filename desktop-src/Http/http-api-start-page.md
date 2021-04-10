---
title: HTTP 伺服器 API \(英文\)
description: HTTP 伺服器 API 可讓應用程式透過 HTTP 進行通訊，而不需要使用 Microsoft Internet information Server (IIS) 。
ms.assetid: ef18716c-7511-4c8a-99bc-28369c3e46f4
keywords:
- HTTP 伺服器 API \(英文\)
- HTTP 伺服器 API、起始頁
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8f99045b24d0ef79c267615791c62da50ed8e40
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104092723"
---
# <a name="http-server-api"></a>HTTP 伺服器 API \(英文\)

## <a name="purpose"></a>目的

HTTP 伺服器 API 可讓應用程式透過 HTTP 進行通訊，而不需要使用 Microsoft Internet information Server (IIS) 。 應用程式可以註冊以接收特定 Url 的 HTTP 要求、接收 HTTP 要求，以及傳送 HTTP 回應。 HTTP 伺服器 API 包含 SSL 支援，讓應用程式可以透過安全的 HTTP 連線來交換資料，而不需要 IIS。 它也是設計來處理 i/o 完成通訊埠。

## <a name="developer-audience"></a>開發人員對象

此 API 是設計來供 C/c + + 程式設計人員使用。

## <a name="run-time-requirements"></a>執行階段需求求

Windows Server 2003 作業系統和 Windows XP Service Pack 2 (SP2) 支援 HTTP 伺服器 API。 請注意，在 Windows XP SP2 上執行的 Microsoft IIS 5 無法與其他同時執行的 HTTP 應用程式共用埠80。

## <a name="in-this-section"></a>本節內容



| 主題                                                                           | 描述                                                                                             |
|---------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------|
| [關於 HTTP 伺服器 API](about-http-server-api.md)<br/>                   | 關於 HTTP 的一般資訊。<br/>                                                              |
| [使用 HTTP 伺服器 API](using-http-server-api.md)<br/>                   | 使用 HTTP 的程式指南。<br/>                                                             |
| [HTTP 伺服器 API 參考](http-server-api-reference.md)<br/>           | 可在 HTTP 中使用的特定函式、結構和列舉類型的檔。<br/>    |
| [HTTP 伺服器範例應用程式](http-server-sample-application.md)<br/> | 示範如何使用 HTTP 伺服器 API 來執行伺服器端工作的範例應用程式。<br/> |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Windows HTTP 服務 (WinHTTP) ](/windows/desktop/WinHttp/winhttp-start-page)
</dt> </dl>

 

