---
title: WebSocket 通訊協定元件 API
description: WebSocket 通訊協定元件 API
ms.assetid: ae73fd5e-9715-448c-b7ca-898f2705e228
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c16290a7af5b5fea406e5f47c0db718d775e4d17
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108088816"
---
# <a name="websocket-protocol-component-api"></a><span data-ttu-id="f4b56-103">WebSocket 通訊協定元件 API</span><span class="sxs-lookup"><span data-stu-id="f4b56-103">WebSocket Protocol Component API</span></span>

## <a name="purpose"></a><span data-ttu-id="f4b56-104">目的</span><span class="sxs-lookup"><span data-stu-id="f4b56-104">Purpose</span></span>

<span data-ttu-id="f4b56-105">WebSocket 通訊協定元件 API 可透過 HTTP （可在現有的網路媒介之間運作）來啟用非同步雙向通道。</span><span class="sxs-lookup"><span data-stu-id="f4b56-105">The WebSocket Protocol Component API enables asynchronous, bi-directional communication channels over HTTP that work across existing network intermediaries.</span></span> <span data-ttu-id="f4b56-106">使用 WebSocket 通訊協定元件 API 時，用戶端會使用 HTTP 來與伺服器通訊，然後再切換到使用 HTTP 分層式 (的基礎通訊協定，例如 TCP 或 SSL) 。</span><span class="sxs-lookup"><span data-stu-id="f4b56-106">With the WebSocket Protocol Component API, a client uses HTTP to communicate with a server, and then both sides switch to using the underlying protocol that HTTP was layered on (such as TCP or SSL).</span></span> <span data-ttu-id="f4b56-107">目標是先使用 HTTP 來跨越網路媒介，然後使用為雙向應用程式通訊所建立的端對端基礎 TCP/SSL 通道。</span><span class="sxs-lookup"><span data-stu-id="f4b56-107">The goal is to first use HTTP to traverse over network intermediaries, and then use the established end-to-end underlying TCP/SSL channel for bi-directional application communication.</span></span> <span data-ttu-id="f4b56-108">WebSocket 通訊協定 \[ [WSPROTO](https://tools.ietf.org/html/rfc6455) \] 是在 IETF 定義，而相關聯的 JAVAscript API \[ [W3CAPI](https://dev.w3.org/html5/websockets/) \] 則是在 W3C 定義。</span><span class="sxs-lookup"><span data-stu-id="f4b56-108">The WebSocket protocol \[[WSPROTO](https://tools.ietf.org/html/rfc6455)\] is defined at the IETF, while an associated Javascript API \[[W3CAPI](https://dev.w3.org/html5/websockets/)\] is defined at the W3C.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="f4b56-109">本節內容</span><span class="sxs-lookup"><span data-stu-id="f4b56-109">In this section</span></span>



| <span data-ttu-id="f4b56-110">主題</span><span class="sxs-lookup"><span data-stu-id="f4b56-110">Topic</span></span>                                                                                                          | <span data-ttu-id="f4b56-111">描述</span><span class="sxs-lookup"><span data-stu-id="f4b56-111">Description</span></span>                                                                 |
|----------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| [<span data-ttu-id="f4b56-112">**WebSocket 通訊協定元件 API 資料類型**</span><span class="sxs-lookup"><span data-stu-id="f4b56-112">**WebSocket Protocol Component API Data Types**</span></span>](web-socket-protocol-component-api-data-types.md)<br/> | <span data-ttu-id="f4b56-113">WebSocket 通訊協定元件 API 會定義這些資料類型。</span><span class="sxs-lookup"><span data-stu-id="f4b56-113">The WebSocket Protocol Component API defines these data types.</span></span><br/>   |
| [<span data-ttu-id="f4b56-114">WebSocket 通訊協定元件 API 列舉</span><span class="sxs-lookup"><span data-stu-id="f4b56-114">WebSocket Protocol Component API Enumerations</span></span>](web-socket-protocol-component-api-enumerations.md)<br/> | <span data-ttu-id="f4b56-115">WebSocket 通訊協定元件 API 會定義這些列舉。</span><span class="sxs-lookup"><span data-stu-id="f4b56-115">The WebSocket Protocol Component API defines these enumerations.</span></span><br/> |
| [<span data-ttu-id="f4b56-116">WebSocket 通訊協定元件 API 函數</span><span class="sxs-lookup"><span data-stu-id="f4b56-116">WebSocket Protocol Component API Functions</span></span>](web-socket-protocol-component-api-functions.md)<br/>       | <span data-ttu-id="f4b56-117">WebSocket 通訊協定元件 API 會定義這些函式。</span><span class="sxs-lookup"><span data-stu-id="f4b56-117">The WebSocket Protocol Component API defines these functions.</span></span><br/>    |
| [<span data-ttu-id="f4b56-118">WebSocket 通訊協定元件 API 結構</span><span class="sxs-lookup"><span data-stu-id="f4b56-118">WebSocket Protocol Component API Structures</span></span>](web-socket-protocol-component-api-structures.md)<br/>     | <span data-ttu-id="f4b56-119">WebSocket 通訊協定元件 API 會定義這些結構。</span><span class="sxs-lookup"><span data-stu-id="f4b56-119">The WebSocket Protocol Component API defines these structures.</span></span><br/>   |



 

## <a name="developer-audience"></a><span data-ttu-id="f4b56-120">開發人員對象</span><span class="sxs-lookup"><span data-stu-id="f4b56-120">Developer audience</span></span>

<span data-ttu-id="f4b56-121">WebSocket 通訊協定元件 API 是設計來供 C/c + + 程式設計人員使用。</span><span class="sxs-lookup"><span data-stu-id="f4b56-121">The WebSocket Protocol Component API is designed for use by use by C/C++ programmers.</span></span> <span data-ttu-id="f4b56-122">需要熟悉 HTTP 和 Windows 網路功能。</span><span class="sxs-lookup"><span data-stu-id="f4b56-122">Familiarity with HTTP and Windows networking is required.</span></span>

> [!Note]  
> <span data-ttu-id="f4b56-123">在 Windows 上使用 WebSocket 通訊協定的慣用方法是透過 [WINDOWS HTTP 服務 (WinHTTP) API](/windows/desktop/WinHttp/winhttp-start-page) 或 [windows. socket 命名空間](/uwp/api/Windows.Networking.Sockets)。</span><span class="sxs-lookup"><span data-stu-id="f4b56-123">The preferred way to use the WebSocket protocol on Windows is through the [Windows HTTP Services (WinHTTP) API](/windows/desktop/WinHttp/winhttp-start-page) or the [Windows.Networking.Sockets namespace](/uwp/api/Windows.Networking.Sockets).</span></span>

 

## <a name="run-time-requirements"></a><span data-ttu-id="f4b56-124">執行階段需求求</span><span class="sxs-lookup"><span data-stu-id="f4b56-124">Run-time requirements</span></span>

<span data-ttu-id="f4b56-125">WebSocket 通訊協定元件 API 需要 Windows 8 和更新版本的 Windows 作業系統。</span><span class="sxs-lookup"><span data-stu-id="f4b56-125">The WebSocket Protocol Component API requires Windows 8 and later versions of the Windows operating system.</span></span> <span data-ttu-id="f4b56-126">您可以透過 websocket.dll 動態連結 Api。</span><span class="sxs-lookup"><span data-stu-id="f4b56-126">The APIs can be dynamically linked through websocket.dll.</span></span>

> [!Note]  
> <span data-ttu-id="f4b56-127">websocket.dll 提供與用戶端和伺服器交握相關的 HTTP 標頭的支援、驗證接收的交握資料，以及剖析 WebSocket 資料串流。</span><span class="sxs-lookup"><span data-stu-id="f4b56-127">websocket.dll provides support for client and server handshake related HTTP headers, verifies received handshake data, and parses the WebSocket data stream.</span></span> <span data-ttu-id="f4b56-128">它不會處理任何 HTTP 特定的作業 (重新導向、驗證、proxy 支援) 也不會執行任何 i/o 作業 (傳送或接收 WebSocket 串流位元組) 。</span><span class="sxs-lookup"><span data-stu-id="f4b56-128">It does not handle any HTTP-specific operations (redirection, authentication, proxy support) nor perform any I/O operations (sending or receiving WebSocket stream bytes).</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="f4b56-129">相關主題</span><span class="sxs-lookup"><span data-stu-id="f4b56-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f4b56-130">HTTP</span><span class="sxs-lookup"><span data-stu-id="f4b56-130">HTTP</span></span>](/windows/desktop/Http/http-api-start-page)
</dt> <dt>

[<span data-ttu-id="f4b56-131">Windows HTTP 服務 (WinHTTP) </span><span class="sxs-lookup"><span data-stu-id="f4b56-131">Windows HTTP Services (WinHTTP)</span></span>](/windows/desktop/WinHttp/winhttp-start-page)
</dt> </dl>

 

