---
title: WebSocket 通訊協定元件 API
description: .
ms.assetid: ae73fd5e-9715-448c-b7ca-898f2705e228
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24edd74fe87185db498e6309a7fda5fa091c7d60
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104092920"
---
# <a name="websocket-protocol-component-api"></a>WebSocket 通訊協定元件 API

## <a name="purpose"></a>目的

WebSocket 通訊協定元件 API 可透過 HTTP （可在現有的網路媒介之間運作）來啟用非同步雙向通道。 使用 WebSocket 通訊協定元件 API 時，用戶端會使用 HTTP 來與伺服器通訊，然後再切換到使用 HTTP 分層式 (的基礎通訊協定，例如 TCP 或 SSL) 。 目標是先使用 HTTP 來跨越網路媒介，然後使用為雙向應用程式通訊所建立的端對端基礎 TCP/SSL 通道。 WebSocket 通訊協定 \[ [WSPROTO](https://tools.ietf.org/html/rfc6455) \] 是在 IETF 定義，而相關聯的 JAVAscript API \[ [W3CAPI](https://dev.w3.org/html5/websockets/) \] 則是在 W3C 定義。

## <a name="in-this-section"></a>本節內容



| 主題                                                                                                          | 描述                                                                 |
|----------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| [**WebSocket 通訊協定元件 API 資料類型**](web-socket-protocol-component-api-data-types.md)<br/> | WebSocket 通訊協定元件 API 會定義這些資料類型。<br/>   |
| [WebSocket 通訊協定元件 API 列舉](web-socket-protocol-component-api-enumerations.md)<br/> | WebSocket 通訊協定元件 API 會定義這些列舉。<br/> |
| [WebSocket 通訊協定元件 API 函數](web-socket-protocol-component-api-functions.md)<br/>       | WebSocket 通訊協定元件 API 會定義這些函式。<br/>    |
| [WebSocket 通訊協定元件 API 結構](web-socket-protocol-component-api-structures.md)<br/>     | WebSocket 通訊協定元件 API 會定義這些結構。<br/>   |



 

## <a name="developer-audience"></a>開發人員對象

WebSocket 通訊協定元件 API 是設計來供 C/c + + 程式設計人員使用。 需要熟悉 HTTP 和 Windows 網路功能。

> [!Note]  
> 在 Windows 上使用 WebSocket 通訊協定的慣用方法是透過 [WINDOWS HTTP 服務 (WinHTTP) API](/windows/desktop/WinHttp/winhttp-start-page) 或 [windows. socket 命名空間](/uwp/api/Windows.Networking.Sockets)。

 

## <a name="run-time-requirements"></a>執行階段需求求

WebSocket 通訊協定元件 API 需要 Windows 8 和更新版本的 Windows 作業系統。 您可以透過 websocket.dll 動態連結 Api。

> [!Note]  
> websocket.dll 提供與用戶端和伺服器交握相關的 HTTP 標頭的支援、驗證接收的交握資料，以及剖析 WebSocket 資料串流。 它不會處理任何 HTTP 特定的作業 (重新導向、驗證、proxy 支援) 也不會執行任何 i/o 作業 (傳送或接收 WebSocket 串流位元組) 。

 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[HTTP](/windows/desktop/Http/http-api-start-page)
</dt> <dt>

[Windows HTTP 服務 (WinHTTP) ](/windows/desktop/WinHttp/winhttp-start-page)
</dt> </dl>

 

