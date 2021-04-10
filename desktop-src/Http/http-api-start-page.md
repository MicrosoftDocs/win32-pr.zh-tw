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
# <a name="http-server-api"></a><span data-ttu-id="e3e47-105">HTTP 伺服器 API \(英文\)</span><span class="sxs-lookup"><span data-stu-id="e3e47-105">HTTP Server API</span></span>

## <a name="purpose"></a><span data-ttu-id="e3e47-106">目的</span><span class="sxs-lookup"><span data-stu-id="e3e47-106">Purpose</span></span>

<span data-ttu-id="e3e47-107">HTTP 伺服器 API 可讓應用程式透過 HTTP 進行通訊，而不需要使用 Microsoft Internet information Server (IIS) 。</span><span class="sxs-lookup"><span data-stu-id="e3e47-107">The HTTP Server API enables applications to communicate over HTTP without using Microsoft Internet Information Server (IIS).</span></span> <span data-ttu-id="e3e47-108">應用程式可以註冊以接收特定 Url 的 HTTP 要求、接收 HTTP 要求，以及傳送 HTTP 回應。</span><span class="sxs-lookup"><span data-stu-id="e3e47-108">Applications can register to receive HTTP requests for particular URLs, receive HTTP requests, and send HTTP responses.</span></span> <span data-ttu-id="e3e47-109">HTTP 伺服器 API 包含 SSL 支援，讓應用程式可以透過安全的 HTTP 連線來交換資料，而不需要 IIS。</span><span class="sxs-lookup"><span data-stu-id="e3e47-109">The HTTP Server API includes SSL support so that applications can exchange data over secure HTTP connections without IIS.</span></span> <span data-ttu-id="e3e47-110">它也是設計來處理 i/o 完成通訊埠。</span><span class="sxs-lookup"><span data-stu-id="e3e47-110">It is also designed to work with I/O completion ports.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="e3e47-111">開發人員對象</span><span class="sxs-lookup"><span data-stu-id="e3e47-111">Developer audience</span></span>

<span data-ttu-id="e3e47-112">此 API 是設計來供 C/c + + 程式設計人員使用。</span><span class="sxs-lookup"><span data-stu-id="e3e47-112">This API is designed for use by C/C++ programmers.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="e3e47-113">執行階段需求求</span><span class="sxs-lookup"><span data-stu-id="e3e47-113">Run-time requirements</span></span>

<span data-ttu-id="e3e47-114">Windows Server 2003 作業系統和 Windows XP Service Pack 2 (SP2) 支援 HTTP 伺服器 API。</span><span class="sxs-lookup"><span data-stu-id="e3e47-114">The HTTP Server API is supported on Windows Server 2003 operating systems and on Windows XP with Service Pack 2 (SP2).</span></span> <span data-ttu-id="e3e47-115">請注意，在 Windows XP SP2 上執行的 Microsoft IIS 5 無法與其他同時執行的 HTTP 應用程式共用埠80。</span><span class="sxs-lookup"><span data-stu-id="e3e47-115">Be aware that Microsoft IIS 5 running on Windows XP with SP2 is not able to share port 80 with other HTTP applications running simultaneously.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="e3e47-116">本節內容</span><span class="sxs-lookup"><span data-stu-id="e3e47-116">In this section</span></span>



| <span data-ttu-id="e3e47-117">主題</span><span class="sxs-lookup"><span data-stu-id="e3e47-117">Topic</span></span>                                                                           | <span data-ttu-id="e3e47-118">描述</span><span class="sxs-lookup"><span data-stu-id="e3e47-118">Description</span></span>                                                                                             |
|---------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e3e47-119">關於 HTTP 伺服器 API</span><span class="sxs-lookup"><span data-stu-id="e3e47-119">About HTTP Server API</span></span>](about-http-server-api.md)<br/>                   | <span data-ttu-id="e3e47-120">關於 HTTP 的一般資訊。</span><span class="sxs-lookup"><span data-stu-id="e3e47-120">General information about HTTP.</span></span><br/>                                                              |
| [<span data-ttu-id="e3e47-121">使用 HTTP 伺服器 API</span><span class="sxs-lookup"><span data-stu-id="e3e47-121">Using HTTP Server API</span></span>](using-http-server-api.md)<br/>                   | <span data-ttu-id="e3e47-122">使用 HTTP 的程式指南。</span><span class="sxs-lookup"><span data-stu-id="e3e47-122">Procedural guide for using HTTP.</span></span><br/>                                                             |
| [<span data-ttu-id="e3e47-123">HTTP 伺服器 API 參考</span><span class="sxs-lookup"><span data-stu-id="e3e47-123">HTTP Server API Reference</span></span>](http-server-api-reference.md)<br/>           | <span data-ttu-id="e3e47-124">可在 HTTP 中使用的特定函式、結構和列舉類型的檔。</span><span class="sxs-lookup"><span data-stu-id="e3e47-124">Documentation of specific functions, structures, and enumeration types available in HTTP.</span></span><br/>    |
| [<span data-ttu-id="e3e47-125">HTTP 伺服器範例應用程式</span><span class="sxs-lookup"><span data-stu-id="e3e47-125">HTTP Server Sample Application</span></span>](http-server-sample-application.md)<br/> | <span data-ttu-id="e3e47-126">示範如何使用 HTTP 伺服器 API 來執行伺服器端工作的範例應用程式。</span><span class="sxs-lookup"><span data-stu-id="e3e47-126">A sample application that shows how to use the HTTP Server API to perform server-side tasks.</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="e3e47-127">相關主題</span><span class="sxs-lookup"><span data-stu-id="e3e47-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e3e47-128">Windows HTTP 服務 (WinHTTP) </span><span class="sxs-lookup"><span data-stu-id="e3e47-128">Windows HTTP Services (WinHTTP)</span></span>](/windows/desktop/WinHttp/winhttp-start-page)
</dt> </dl>

 

