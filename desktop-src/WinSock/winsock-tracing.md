---
description: Winsock 追蹤
ms.assetid: 0c430fc2-28e7-4537-a887-4c36d24fedee
title: Winsock 追蹤
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 803be6220d4d2d440811033786b0f043fab0ff9d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106991997"
---
# <a name="winsock-tracing"></a><span data-ttu-id="68027-103">Winsock 追蹤</span><span class="sxs-lookup"><span data-stu-id="68027-103">Winsock Tracing</span></span>

## <a name="introduction"></a><span data-ttu-id="68027-104">簡介</span><span class="sxs-lookup"><span data-stu-id="68027-104">Introduction</span></span>

<span data-ttu-id="68027-105">Winsock 追蹤是一項疑難排解功能，可以在零售二進位檔中啟用，以追蹤某些 Windows 通訊端事件的額外負荷。</span><span class="sxs-lookup"><span data-stu-id="68027-105">Winsock tracing is a troubleshooting feature that can be enabled in retail binaries to trace certain Windows socket events with minimal overhead.</span></span> <span data-ttu-id="68027-106">將零售追蹤新增至 Windows 通訊端的目標是要讓開發人員和產品支援提供更佳的診斷功能。</span><span class="sxs-lookup"><span data-stu-id="68027-106">The goal of adding retail tracing to Windows Sockets is to allow for better diagnostic capabilities for developers and product support.</span></span> <span data-ttu-id="68027-107">Winsock 網路事件追蹤支援 IPv4 和 IPv6 應用程式的追蹤通訊端作業。</span><span class="sxs-lookup"><span data-stu-id="68027-107">Winsock network event tracing supports tracing socket operations for IPv4 and IPv6 applications.</span></span> <span data-ttu-id="68027-108">Winsock 目錄變更追蹤支援追蹤對 Winsock 類別目錄所做的變更， (Lsp) 的分層服務提供者。</span><span class="sxs-lookup"><span data-stu-id="68027-108">Winsock catalog change tracing supports tracing changes made to the Winsock catalog by layered service providers (LSPs).</span></span> <span data-ttu-id="68027-109">Windows Vista 和更新版本支援 Winsock 追蹤。</span><span class="sxs-lookup"><span data-stu-id="68027-109">Winsock tracing is supported on Windows Vista and later.</span></span>

> [!Note]  
> <span data-ttu-id="68027-110">已淘汰分層服務提供者。</span><span class="sxs-lookup"><span data-stu-id="68027-110">Layered Service Providers are deprecated.</span></span> <span data-ttu-id="68027-111">從 Windows 8 和 Windows Server 2012 開始，請使用 [Windows 篩選平台](../fwp/windows-filtering-platform-start-page.md)。</span><span class="sxs-lookup"><span data-stu-id="68027-111">Starting with Windows 8 and Windows Server 2012, use [Windows Filtering Platform](../fwp/windows-filtering-platform-start-page.md).</span></span>

 

<span data-ttu-id="68027-112">當通訊端發生未預期的錯誤時，診斷問題的主要線索就是傳回的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="68027-112">When an unexpected error occurs on a socket, the main clue to diagnose the problem is the error code returned.</span></span> <span data-ttu-id="68027-113">傳回的錯誤碼通常不會解釋發生錯誤的原因，特別是當基礎網路傳輸起始錯誤時。</span><span class="sxs-lookup"><span data-stu-id="68027-113">Very often, the returned error code does not explain why the error happened, especially when the error is initiated by the underlying network transport.</span></span> <span data-ttu-id="68027-114">Winsock 追蹤提供更詳細的追蹤層級，可記錄其他資訊來攔截緩衝區損毀和寫入不良的應用程式。</span><span class="sxs-lookup"><span data-stu-id="68027-114">Winsock tracing provides a more verbose tracing level which can log additional information to catch buffer corruption and poorly written applications.</span></span>

<span data-ttu-id="68027-115">Winsock 追蹤會使用 Windows 的事件追蹤 (ETW) 是作業系統所提供的一般用途高速追蹤功能。</span><span class="sxs-lookup"><span data-stu-id="68027-115">Winsock tracing uses Event Tracing for Windows (ETW), a general-purpose, high-speed tracing facility provided by the operating system.</span></span> <span data-ttu-id="68027-116">ETW 使用在核心中實作為緩衝和記錄機制，為使用者模式應用程式與核心模式設備磁碟機所引發的事件提供追蹤機制。</span><span class="sxs-lookup"><span data-stu-id="68027-116">Using a buffering and logging mechanism implemented in the kernel, ETW provides a tracing mechanism for events raised by both user-mode applications and kernel-mode device drivers.</span></span> <span data-ttu-id="68027-117">此外，ETW 還可讓您以動態方式啟用和停用記錄，讓您輕鬆地在生產環境中執行詳細追蹤，而不需要重新開機或重新開機應用程式。</span><span class="sxs-lookup"><span data-stu-id="68027-117">Additionally, ETW gives you the ability to enable and disable logging dynamically, making it easy to perform detailed tracing in production environments without requiring reboots or application restarts.</span></span> <span data-ttu-id="68027-118">記錄機制會使用由非同步寫入器執行緒寫入磁片的緩衝區。</span><span class="sxs-lookup"><span data-stu-id="68027-118">The logging mechanism uses buffers that are written to disk by an asynchronous writer thread.</span></span> <span data-ttu-id="68027-119">這可讓大型伺服器應用程式以最少的干擾來寫入事件。</span><span class="sxs-lookup"><span data-stu-id="68027-119">This allows large-scale server applications to write events with minimum disturbance.</span></span> <span data-ttu-id="68027-120">ETW 首次在 Windows 2000 上引進。</span><span class="sxs-lookup"><span data-stu-id="68027-120">ETW was first introduced on Windows 2000.</span></span> <span data-ttu-id="68027-121">Windows Vista 和更新版本已新增使用 ETW 進行 Winsock 追蹤的支援。</span><span class="sxs-lookup"><span data-stu-id="68027-121">Support for Winsock tracing using ETW was added on Windows Vista and later.</span></span> <span data-ttu-id="68027-122">如需 ETW 的一般資訊，請參閱 [使用 Etw 改善偵錯工具和效能微調](/archive/msdn-magazine/2007/april/event-tracing-improve-debugging-and-performance-tuning-with-etw)。</span><span class="sxs-lookup"><span data-stu-id="68027-122">For general information on ETW, see [Improve Debugging And Performance Tuning With ETW](/archive/msdn-magazine/2007/april/event-tracing-improve-debugging-and-performance-tuning-with-etw).</span></span>

<span data-ttu-id="68027-123">您只能針對在電腦上執行的所有進程和執行緒，在作業系統層級啟用 Winsock 追蹤。</span><span class="sxs-lookup"><span data-stu-id="68027-123">Winsock tracing can only be enabled at the operating system level for all processes and threads running on a computer.</span></span> <span data-ttu-id="68027-124">目前只能針對單一進程或執行緒啟用 Winsock 追蹤。</span><span class="sxs-lookup"><span data-stu-id="68027-124">Winsock tracing currently cannot be enabled for just a single process or thread.</span></span> <span data-ttu-id="68027-125">啟用 Winsock 網路事件追蹤時，會追蹤電腦上 (IPv4 和 IPv6) 的所有通訊端應用程式。</span><span class="sxs-lookup"><span data-stu-id="68027-125">When Winsock network event tracing is enabled, all socket applications (both IPv4 and IPv6) on a computer are traced.</span></span>

<span data-ttu-id="68027-126">下列主題會更詳細地說明 Winsock 追蹤：</span><span class="sxs-lookup"><span data-stu-id="68027-126">The following topics describe Winsock tracing in more detail:</span></span>

-   [<span data-ttu-id="68027-127">Winsock 追蹤層級</span><span class="sxs-lookup"><span data-stu-id="68027-127">Winsock Tracing Levels</span></span>](winsock-tracing-levels.md)
-   [<span data-ttu-id="68027-128">Winsock 追蹤的控制權</span><span class="sxs-lookup"><span data-stu-id="68027-128">Control of Winsock Tracing</span></span>](control-of-winsock-tracing.md)
-   [<span data-ttu-id="68027-129">Winsock 網路事件追蹤詳細資料</span><span class="sxs-lookup"><span data-stu-id="68027-129">Winsock Network Event Tracing Details</span></span>](winsock-tracing-event-details.md)
-   [<span data-ttu-id="68027-130">Winsock 目錄變更追蹤詳細資料</span><span class="sxs-lookup"><span data-stu-id="68027-130">Winsock Catalog Change Tracing Details</span></span>](winsock-layered-service-provider-tracing-event-details.md)

## <a name="related-topics"></a><span data-ttu-id="68027-131">相關主題</span><span class="sxs-lookup"><span data-stu-id="68027-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="68027-132">使用 ETW 改善偵錯和效能調整</span><span class="sxs-lookup"><span data-stu-id="68027-132">Improve Debugging And Performance Tuning With ETW</span></span>](/archive/msdn-magazine/2007/april/event-tracing-improve-debugging-and-performance-tuning-with-etw)
</dt> <dt>

[<span data-ttu-id="68027-133">Debug 和 Trace 設備</span><span class="sxs-lookup"><span data-stu-id="68027-133">Debug and Trace Facilities</span></span>](debug-and-trace-facilities-2.md)
</dt> </dl>

 

 
