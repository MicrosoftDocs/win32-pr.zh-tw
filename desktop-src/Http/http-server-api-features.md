---
title: HTTP 伺服器 API 功能
description: 本主題支援和不支援的 HTTP 伺服器 API 功能。
ms.assetid: 448fe5a5-e79f-4c3a-aa76-94cff988f24f
keywords:
- HTTP 伺服器 API 功能
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48d5f529811b08999d6e1cfffa99fc85288ec471
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104301836"
---
# <a name="http-server-api-features"></a><span data-ttu-id="ecd7b-104">HTTP 伺服器 API 功能</span><span class="sxs-lookup"><span data-stu-id="ecd7b-104">HTTP Server API Features</span></span>

<span data-ttu-id="ecd7b-105">下列清單描述 HTTP 伺服器 API 支援和不支援的功能。</span><span class="sxs-lookup"><span data-stu-id="ecd7b-105">The following lists describe supported and unsupported features of the HTTP Server API.</span></span>

## <a name="features-supported"></a><span data-ttu-id="ecd7b-106">支援的功能</span><span class="sxs-lookup"><span data-stu-id="ecd7b-106">Features Supported</span></span>

<span data-ttu-id="ecd7b-107">HTTP 支援下列功能：</span><span class="sxs-lookup"><span data-stu-id="ecd7b-107">HTTP supports the following features:</span></span>

-   <span data-ttu-id="ecd7b-108">HTTP v1.0 和 v1.1 伺服器功能。</span><span class="sxs-lookup"><span data-stu-id="ecd7b-108">HTTP v1.0 and v1.1 server functionality.</span></span>
-   <span data-ttu-id="ecd7b-109">安全通訊端層 3.0 (SSL) 支援用戶端和伺服器憑證。</span><span class="sxs-lookup"><span data-stu-id="ecd7b-109">Secure Sockets Layer 3.0 (SSL) with support for client and server certificates.</span></span>
-   <span data-ttu-id="ecd7b-110">要在後續回應中使用的資料片段快取。</span><span class="sxs-lookup"><span data-stu-id="ecd7b-110">Caching of data fragments for use in subsequent responses.</span></span>
-   <span data-ttu-id="ecd7b-111">支援 IPv6 和 IPv4 定址。</span><span class="sxs-lookup"><span data-stu-id="ecd7b-111">Support for IPv6 and IPv4 addressing.</span></span>
-   <span data-ttu-id="ecd7b-112">應用程式安全性的 URL 命名空間保留專案。</span><span class="sxs-lookup"><span data-stu-id="ecd7b-112">URL namespace reservations for application security.</span></span>
-   <span data-ttu-id="ecd7b-113">所有物件的真正控制碼。</span><span class="sxs-lookup"><span data-stu-id="ecd7b-113">True handles for all objects.</span></span>
-   <span data-ttu-id="ecd7b-114">同步和非同步 i/o 模型。</span><span class="sxs-lookup"><span data-stu-id="ecd7b-114">Synchronous and asynchronous I/O models.</span></span>
-   <span data-ttu-id="ecd7b-115">在64位 Windows 上執行的電腦上支援 WOW64，從 Windows Server 2003 Service Pack 1 開始 (SP1) 。</span><span class="sxs-lookup"><span data-stu-id="ecd7b-115">Support for WOW64 on computers running on 64-bit Windows starting with Windows Server 2003 with Service Pack 1 (SP1).</span></span>

## <a name="features-not-supported"></a><span data-ttu-id="ecd7b-116">不支援的功能</span><span class="sxs-lookup"><span data-stu-id="ecd7b-116">Features Not Supported</span></span>

<span data-ttu-id="ecd7b-117">HTTP 伺服器 API 不支援下列功能：</span><span class="sxs-lookup"><span data-stu-id="ecd7b-117">The HTTP Server API does not support the following functionality:</span></span>

-   <span data-ttu-id="ecd7b-118">HTTP 伺服器 API 不會根據 HTTP 要求標頭的內容執行用戶端或伺服器驗證。</span><span class="sxs-lookup"><span data-stu-id="ecd7b-118">The HTTP Server API does not perform client or server authentication based on the contents of the HTTP request headers.</span></span> <span data-ttu-id="ecd7b-119">應用程式必須執行任何必要的驗證。</span><span class="sxs-lookup"><span data-stu-id="ecd7b-119">Any required authentication must be implemented by the application.</span></span>
-   <span data-ttu-id="ecd7b-120">Windows Server 2003 以及 Windows XP Service Pack 2 (SP2) 及更早版本，不支援在64位 Windows 上執行的電腦上的 WOW64。</span><span class="sxs-lookup"><span data-stu-id="ecd7b-120">WOW64 on computers running on 64-bit Windows is not supported on Windows Server 2003, and Windows XP with Service Pack 2 (SP2) and earlier.</span></span>
-   <span data-ttu-id="ecd7b-121">HTTP 伺服器 API 不支援記錄 HTTP 要求和回應。</span><span class="sxs-lookup"><span data-stu-id="ecd7b-121">The HTTP Server API does not support logging HTTP requests and responses.</span></span>
-   <span data-ttu-id="ecd7b-122">HTTP 伺服器 API 不會將傳出的 HTTP 回應區塊。</span><span class="sxs-lookup"><span data-stu-id="ecd7b-122">The HTTP Server API does not chunk outgoing HTTP responses.</span></span> <span data-ttu-id="ecd7b-123">如果需要，應用程式必須執行回應區塊化。</span><span class="sxs-lookup"><span data-stu-id="ecd7b-123">The application must implement response chunking if required.</span></span>

 

 




