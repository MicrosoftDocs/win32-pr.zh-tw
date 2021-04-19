---
description: 深入瞭解：記憶體管理追蹤事件
ms.assetid: D53BD414-F140-496E-884F-5A4EC4F0AAC4
title: 記憶體管理追蹤事件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73ca05260b6c29ecae765c047691b81a26116fb9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106997265"
---
# <a name="memory-management-tracing-events"></a><span data-ttu-id="bbf73-103">記憶體管理追蹤事件</span><span class="sxs-lookup"><span data-stu-id="bbf73-103">Memory Management Tracing Events</span></span>

<span data-ttu-id="bbf73-104">本節說明特定記憶體管理追蹤事件詳細資料的詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="bbf73-104">This section describes detailed information on specific Memory management tracing event details.</span></span>

<span data-ttu-id="bbf73-105">記憶體管理追蹤是一個疑難排解功能，可在零售二進位檔中啟用，以盡可能減少額外負荷來追蹤特定的記憶體管理事件。</span><span class="sxs-lookup"><span data-stu-id="bbf73-105">Memory management tracing is a troubleshooting feature that can be enabled in retail binaries to trace certain memory management events with minimal overhead.</span></span> <span data-ttu-id="bbf73-106">這項功能可讓開發人員和產品支援獲得更佳的診斷功能。</span><span class="sxs-lookup"><span data-stu-id="bbf73-106">This feature allows for better diagnostic capabilities for developers and product support.</span></span> <span data-ttu-id="bbf73-107">記憶體管理事件追蹤支援追蹤堆積配置、重新配置和可用的作業。</span><span class="sxs-lookup"><span data-stu-id="bbf73-107">Memory management event tracing supports tracing heap allocation, reallocation, and free operations.</span></span>

<span data-ttu-id="bbf73-108">記憶體管理事件追蹤會使用 Windows 的事件追蹤 (ETW) 是作業系統所提供的一般用途高速追蹤功能。</span><span class="sxs-lookup"><span data-stu-id="bbf73-108">Memory management event tracing uses Event Tracing for Windows (ETW), a general-purpose, high-speed tracing facility provided by the operating system.</span></span> <span data-ttu-id="bbf73-109">ETW 針對使用者模式應用程式和核心模式設備磁碟機所引發的事件，提供追蹤機制。</span><span class="sxs-lookup"><span data-stu-id="bbf73-109">ETW provides a tracing mechanism for events raised by both user-mode applications and kernel-mode device drivers.</span></span> <span data-ttu-id="bbf73-110">ETW 可以動態啟用和停用記錄，讓您輕鬆地在生產環境中執行詳細追蹤，而不需要重新開機或重新開機應用程式。</span><span class="sxs-lookup"><span data-stu-id="bbf73-110">ETW can enable and disable logging dynamically, making it easy to perform detailed tracing in production environments without requiring reboots or application restarts.</span></span> <span data-ttu-id="bbf73-111">Windows 7、Windows Server 2008 R2 和更新版本支援使用 ETW 的記憶體管理事件追蹤。</span><span class="sxs-lookup"><span data-stu-id="bbf73-111">Memory management event tracing using ETW is supported on Windows 7 , Windows Server 2008 R2, and later.</span></span> <span data-ttu-id="bbf73-112">如需 ETW 的一般資訊，請參閱 [使用 Etw 改善偵錯工具和效能微調](/archive/msdn-magazine/2007/april/event-tracing-improve-debugging-and-performance-tuning-with-etw)。</span><span class="sxs-lookup"><span data-stu-id="bbf73-112">For general information on ETW, see [Improve Debugging And Performance Tuning With ETW](/archive/msdn-magazine/2007/april/event-tracing-improve-debugging-and-performance-tuning-with-etw).</span></span>

<span data-ttu-id="bbf73-113">下列清單提供每個記憶體管理追蹤事件的詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="bbf73-113">The following list provides detailed information for each memory management tracing event.</span></span> <span data-ttu-id="bbf73-114">如需任何事件的詳細資訊，請按一下事件名稱。</span><span class="sxs-lookup"><span data-stu-id="bbf73-114">For additional information on any event, click the event name.</span></span>



| <span data-ttu-id="bbf73-115">活動名稱</span><span class="sxs-lookup"><span data-stu-id="bbf73-115">Event Name</span></span>                                                  | <span data-ttu-id="bbf73-116">Description</span><span class="sxs-lookup"><span data-stu-id="bbf73-116">Description</span></span>                                                         |
|-------------------------------------------------------------|---------------------------------------------------------------------|
| [<span data-ttu-id="bbf73-117">**ETW \_ 堆積 \_ 事件 \_ 分配**</span><span class="sxs-lookup"><span data-stu-id="bbf73-117">**ETW\_HEAP\_EVENT\_ALLOC**</span></span>](etw-heap-event-alloc.md)     | <span data-ttu-id="bbf73-118">堆積配置作業的記憶體管理追蹤事件。</span><span class="sxs-lookup"><span data-stu-id="bbf73-118">Memory management tracing event for a heap allocation operation.</span></span>    |
| [<span data-ttu-id="bbf73-119">**ETW \_ 堆積 \_ 事件 \_ 可用**</span><span class="sxs-lookup"><span data-stu-id="bbf73-119">**ETW\_HEAP\_EVENT\_FREE**</span></span>](etw-heap-event-free.md)       | <span data-ttu-id="bbf73-120">堆積免費作業的記憶體管理追蹤事件。</span><span class="sxs-lookup"><span data-stu-id="bbf73-120">Memory management tracing event for a heap free operation.</span></span>          |
| [<span data-ttu-id="bbf73-121">**ETW \_ 堆積 \_ 事件 \_ REALLOC**</span><span class="sxs-lookup"><span data-stu-id="bbf73-121">**ETW\_HEAP\_EVENT\_REALLOC**</span></span>](etw-heap-event-realloc.md) | <span data-ttu-id="bbf73-122">堆積重新配置作業的記憶體管理追蹤事件。</span><span class="sxs-lookup"><span data-stu-id="bbf73-122">Memory management tracing event for a heap re-allocation operation.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="bbf73-123">相關主題</span><span class="sxs-lookup"><span data-stu-id="bbf73-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bbf73-124">使用 ETW 改善偵錯和效能調整</span><span class="sxs-lookup"><span data-stu-id="bbf73-124">Improve Debugging And Performance Tuning With ETW</span></span>](/archive/msdn-magazine/2007/april/event-tracing-improve-debugging-and-performance-tuning-with-etw)
</dt> </dl>

 

 
