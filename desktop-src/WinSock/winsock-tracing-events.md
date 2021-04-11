---
description: Winsock 追蹤事件詳細資料。
ms.assetid: 246AE0BE-E8E2-4291-8BF4-577F889F055B
title: Winsock 追蹤事件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aeabd2d06741f8dfa1f47b513a09c941ee1490b6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112988"
---
# <a name="winsock-tracing-events"></a><span data-ttu-id="e066d-103">Winsock 追蹤事件</span><span class="sxs-lookup"><span data-stu-id="e066d-103">Winsock Tracing Events</span></span>

<span data-ttu-id="e066d-104">本節說明特定 Winsock 追蹤事件詳細資料的詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="e066d-104">This section describes detailed information on specific Winsock Tracing Events details.</span></span>

<span data-ttu-id="e066d-105">Winsock 追蹤是一項疑難排解功能，可以在零售二進位檔中啟用，以追蹤某些 Windows 通訊端事件的額外負荷。</span><span class="sxs-lookup"><span data-stu-id="e066d-105">Winsock tracing is a troubleshooting feature that can be enabled in retail binaries to trace certain Windows socket events with minimal overhead.</span></span> <span data-ttu-id="e066d-106">這項功能可讓開發人員和產品支援獲得更佳的診斷功能。</span><span class="sxs-lookup"><span data-stu-id="e066d-106">This feature allows for better diagnostic capabilities for developers and product support.</span></span> <span data-ttu-id="e066d-107">Winsock 網路事件追蹤支援 IPv4 和 IPv6 應用程式的追蹤通訊端作業。</span><span class="sxs-lookup"><span data-stu-id="e066d-107">Winsock network event tracing supports tracing socket operations for IPv4 and IPv6 applications.</span></span> <span data-ttu-id="e066d-108">Winsock 目錄變更追蹤支援追蹤對 Winsock 類別目錄所做的變更， (Lsp) 的分層服務提供者。</span><span class="sxs-lookup"><span data-stu-id="e066d-108">Winsock catalog change tracing supports tracing changes made to the Winsock catalog by layered service providers (LSPs).</span></span>

> [!Note]  
> <span data-ttu-id="e066d-109">已淘汰分層服務提供者。</span><span class="sxs-lookup"><span data-stu-id="e066d-109">Layered Service Providers are deprecated.</span></span> <span data-ttu-id="e066d-110">從 Windows 8 和 Windows Server 2012 開始，請使用 [Windows 篩選平台](../fwp/windows-filtering-platform-start-page.md)。</span><span class="sxs-lookup"><span data-stu-id="e066d-110">Starting with Windows 8 and Windows Server 2012, use [Windows Filtering Platform](../fwp/windows-filtering-platform-start-page.md).</span></span>

 

<span data-ttu-id="e066d-111">Winsock 追蹤會使用 Windows 的事件追蹤 (ETW) 是作業系統所提供的一般用途高速追蹤功能。</span><span class="sxs-lookup"><span data-stu-id="e066d-111">Winsock tracing uses Event Tracing for Windows (ETW), a general-purpose, high-speed tracing facility provided by the operating system.</span></span> <span data-ttu-id="e066d-112">ETW 針對使用者模式應用程式和核心模式設備磁碟機所引發的事件，提供追蹤機制。</span><span class="sxs-lookup"><span data-stu-id="e066d-112">ETW provides a tracing mechanism for events raised by both user-mode applications and kernel-mode device drivers.</span></span> <span data-ttu-id="e066d-113">ETW 可以動態啟用和停用記錄，讓您輕鬆地在生產環境中執行詳細追蹤，而不需要重新開機或重新開機應用程式。</span><span class="sxs-lookup"><span data-stu-id="e066d-113">ETW can enable and disable logging dynamically, making it easy to perform detailed tracing in production environments without requiring reboots or application restarts.</span></span> <span data-ttu-id="e066d-114">Windows Vista 和更新版本已新增使用 ETW 進行 Winsock 追蹤的支援。</span><span class="sxs-lookup"><span data-stu-id="e066d-114">Support for Winsock tracing using ETW was added on Windows Vista and later.</span></span> <span data-ttu-id="e066d-115">如需 ETW 的一般資訊，請參閱 [使用 Etw 改善偵錯工具和效能微調](/archive/msdn-magazine/2007/april/event-tracing-improve-debugging-and-performance-tuning-with-etw)。</span><span class="sxs-lookup"><span data-stu-id="e066d-115">For general information on ETW, see [Improve Debugging And Performance Tuning With ETW](/archive/msdn-magazine/2007/april/event-tracing-improve-debugging-and-performance-tuning-with-etw).</span></span>

<span data-ttu-id="e066d-116">下列清單提供每個 Winsock 追蹤事件的詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="e066d-116">The following list provides detailed information for each Winsock tracing event.</span></span> <span data-ttu-id="e066d-117">如需任何事件的詳細資訊，請按一下事件名稱。</span><span class="sxs-lookup"><span data-stu-id="e066d-117">For additional information on any event, click the event name.</span></span>



| <span data-ttu-id="e066d-118">活動名稱</span><span class="sxs-lookup"><span data-stu-id="e066d-118">Event Name</span></span>                                                            | <span data-ttu-id="e066d-119">Description</span><span class="sxs-lookup"><span data-stu-id="e066d-119">Description</span></span>                                                                               |
|-----------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e066d-120">**AFD \_ 事件 \_ 建立**</span><span class="sxs-lookup"><span data-stu-id="e066d-120">**AFD\_EVENT\_CREATE**</span></span>](afd-event-create.md)                        | <span data-ttu-id="e066d-121">適用于通訊端建立作業的 Winsock 網路追蹤事件。</span><span class="sxs-lookup"><span data-stu-id="e066d-121">Winsock network tracing event for a socket creation operation.</span></span>                            |
| [<span data-ttu-id="e066d-122">**AFD \_ 事件 \_ 關閉**</span><span class="sxs-lookup"><span data-stu-id="e066d-122">**AFD\_EVENT\_CLOSE**</span></span>](afd-event-close.md)                          | <span data-ttu-id="e066d-123">適用于通訊端關閉操作的 Winsock 網路追蹤事件。</span><span class="sxs-lookup"><span data-stu-id="e066d-123">Winsock network tracing event for socket close operation.</span></span>                                 |
| [<span data-ttu-id="e066d-124">**WINSOCK \_ WS2HELP \_ LSP \_ 安裝**</span><span class="sxs-lookup"><span data-stu-id="e066d-124">**WINSOCK\_WS2HELP\_LSP\_INSTALL**</span></span>](winsock-ws2help-lsp-install.md) | <span data-ttu-id="e066d-125">多層式服務提供者的 Winsock 目錄變更事件 (LSP) 安裝作業。</span><span class="sxs-lookup"><span data-stu-id="e066d-125">Winsock catalog change event for a layered service provider (LSP) installation operation.</span></span> |
| [<span data-ttu-id="e066d-126">**WINSOCK \_ WS2HELP \_ LSP \_ 移除**</span><span class="sxs-lookup"><span data-stu-id="e066d-126">**WINSOCK\_WS2HELP\_LSP\_REMOVE**</span></span>](winsock-ws2help-lsp-remove.md)   | <span data-ttu-id="e066d-127">多層式服務提供者的 Winsock 目錄變更事件 (LSP) 移除作業。</span><span class="sxs-lookup"><span data-stu-id="e066d-127">Winsock catalog change event for a layered service provider (LSP) removal operation.</span></span>      |
| [<span data-ttu-id="e066d-128">**WINSOCK \_ WS2HELP \_ LSP \_ DISABLE**</span><span class="sxs-lookup"><span data-stu-id="e066d-128">**WINSOCK\_WS2HELP\_LSP\_DISABLE**</span></span>](winsock-ws2help-lsp-disable.md) | <span data-ttu-id="e066d-129">多層式服務提供者的 Winsock 目錄變更事件 (LSP) 停用作業。</span><span class="sxs-lookup"><span data-stu-id="e066d-129">Winsock catalog change event for a layered service provider (LSP) disable operation.</span></span>      |
| [<span data-ttu-id="e066d-130">**WINSOCK \_ WS2HELP \_ LSP \_ 重設**</span><span class="sxs-lookup"><span data-stu-id="e066d-130">**WINSOCK\_WS2HELP\_LSP\_RESET**</span></span>](winsock-ws2help-lsp-reset.md)     | <span data-ttu-id="e066d-131">Winsock 類別目錄重設作業的 winsock 目錄變更事件。</span><span class="sxs-lookup"><span data-stu-id="e066d-131">Winsock catalog change event for a Winsock catalog reset operation.</span></span>                       |



 

## <a name="related-topics"></a><span data-ttu-id="e066d-132">相關主題</span><span class="sxs-lookup"><span data-stu-id="e066d-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e066d-133">使用 ETW 改善偵錯和效能調整</span><span class="sxs-lookup"><span data-stu-id="e066d-133">Improve Debugging And Performance Tuning With ETW</span></span>](/archive/msdn-magazine/2007/april/event-tracing-improve-debugging-and-performance-tuning-with-etw)
</dt> <dt>

[<span data-ttu-id="e066d-134">Winsock 追蹤</span><span class="sxs-lookup"><span data-stu-id="e066d-134">Winsock Tracing</span></span>](winsock-tracing.md)
</dt> <dt>

[<span data-ttu-id="e066d-135">Winsock 追蹤層級</span><span class="sxs-lookup"><span data-stu-id="e066d-135">Winsock Tracing Levels</span></span>](winsock-tracing-levels.md)
</dt> <dt>

[<span data-ttu-id="e066d-136">Winsock 追蹤的控制權</span><span class="sxs-lookup"><span data-stu-id="e066d-136">Control of Winsock Tracing</span></span>](control-of-winsock-tracing.md)
</dt> <dt>

[<span data-ttu-id="e066d-137">Winsock 網路事件追蹤詳細資料</span><span class="sxs-lookup"><span data-stu-id="e066d-137">Winsock Network Event Tracing Details</span></span>](winsock-tracing-event-details.md)
</dt> <dt>

[<span data-ttu-id="e066d-138">Winsock 目錄變更追蹤詳細資料</span><span class="sxs-lookup"><span data-stu-id="e066d-138">Winsock Catalog Change Tracing Details</span></span>](winsock-layered-service-provider-tracing-event-details.md)
</dt> </dl>

 

 
