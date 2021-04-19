---
description: 許多應用程式會在專屬的錯誤記錄檔中記錄錯誤和事件，每個都有自己的格式和使用者介面。
ms.assetid: 5ec95938-ac5d-4f63-9080-2de71454eb17
title: '事件記錄 (事件記錄) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d9871fdb7c7b81bdf57a8c5de87a0a09d5a0570
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106985311"
---
# <a name="event-logging-event-logging"></a><span data-ttu-id="d82d9-103">事件記錄 (事件記錄) </span><span class="sxs-lookup"><span data-stu-id="d82d9-103">Event Logging (Event Logging)</span></span>

<span data-ttu-id="d82d9-104">許多應用程式會在專屬的錯誤記錄檔中記錄錯誤和事件，每個都有自己的格式和使用者介面。</span><span class="sxs-lookup"><span data-stu-id="d82d9-104">Many applications record errors and events in proprietary error logs, each with their own format and user interface.</span></span> <span data-ttu-id="d82d9-105">不同應用程式中的資料無法輕鬆地合併為一份完整的報告，需要系統管理員或支援代表來檢查各種來源以診斷問題。</span><span class="sxs-lookup"><span data-stu-id="d82d9-105">Data from different applications can't easily be merged into one complete report, requiring system administrators or support representatives to check a variety of sources to diagnose problems.</span></span>

<span data-ttu-id="d82d9-106">事件記錄可為應用程式提供標準、集中式的方式 (以及記錄重要軟體和硬體事件的作業系統) 。</span><span class="sxs-lookup"><span data-stu-id="d82d9-106">Event logging provides a standard, centralized way for applications (and the operating system) to record important software and hardware events.</span></span> <span data-ttu-id="d82d9-107">事件記錄服務會記錄來自各種來源的事件，並將它們儲存在稱為 *事件記錄* 檔的單一集合中。</span><span class="sxs-lookup"><span data-stu-id="d82d9-107">The event logging service records events from various sources and stores them in a single collection called an *event log*.</span></span> <span data-ttu-id="d82d9-108">事件檢視器可讓您查看記錄;程式設計介面也可讓您檢查記錄。</span><span class="sxs-lookup"><span data-stu-id="d82d9-108">The Event Viewer enables you to view logs; the programming interface also enables you to examine logs.</span></span>

-   [<span data-ttu-id="d82d9-109">關於事件記錄</span><span class="sxs-lookup"><span data-stu-id="d82d9-109">About Event Logging</span></span>](about-event-logging.md)
-   [<span data-ttu-id="d82d9-110">使用事件記錄</span><span class="sxs-lookup"><span data-stu-id="d82d9-110">Using Event Logging</span></span>](using-event-logging.md)
-   [<span data-ttu-id="d82d9-111">事件記錄參考</span><span class="sxs-lookup"><span data-stu-id="d82d9-111">Event Logging Reference</span></span>](event-logging-reference.md)

> [!Note]  
> <span data-ttu-id="d82d9-112">事件記錄 API 是針對在 Windows Server 2003、Windows XP 或 Windows 2000 作業系統上執行的應用程式所設計。</span><span class="sxs-lookup"><span data-stu-id="d82d9-112">The Event Logging API was designed for applications that run on the Windows Server 2003, Windows XP, or Windows 2000 operating system.</span></span> <span data-ttu-id="d82d9-113">在 Windows Vista 中，已重新設計事件記錄基礎結構。</span><span class="sxs-lookup"><span data-stu-id="d82d9-113">In Windows Vista, the event logging infrastructure was redesigned.</span></span> <span data-ttu-id="d82d9-114">設計成在 Windows Vista 或更新版本的作業系統上執行的應用程式應該使用 [Windows 事件記錄](/windows/desktop/WES/windows-event-log) 檔來記錄事件。</span><span class="sxs-lookup"><span data-stu-id="d82d9-114">Applications that are designed to run on Windows Vista or later operating systems should use [Windows Event Log](/windows/desktop/WES/windows-event-log) to log events.</span></span>
