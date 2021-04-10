---
description: 發生錯誤時，系統管理員或支援代表必須判斷造成錯誤的原因、嘗試復原遺失的資料，並防止錯誤重複發生。
ms.assetid: 2a625c8a-afa2-484a-a0e3-df3ef774abe4
title: 關於事件記錄
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1104a4b54d2989cb329b665e20fd273766e57209
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104026331"
---
# <a name="about-event-logging"></a><span data-ttu-id="a3160-103">關於事件記錄</span><span class="sxs-lookup"><span data-stu-id="a3160-103">About Event Logging</span></span>

<span data-ttu-id="a3160-104">發生錯誤時，系統管理員或支援代表必須判斷造成錯誤的原因、嘗試復原遺失的資料，並防止錯誤重複發生。</span><span class="sxs-lookup"><span data-stu-id="a3160-104">When an error occurs, the system administrator or support representative must determine what caused the error, attempt to recover any lost data, and prevent the error from recurring.</span></span> <span data-ttu-id="a3160-105">如果應用程式、作業系統和其他系統服務記錄重要事件（例如，記憶體不足的狀況或過多的存取磁片的嘗試），這會很有説明。</span><span class="sxs-lookup"><span data-stu-id="a3160-105">It is helpful if applications, the operating system, and other system services record important events, such as low-memory conditions or excessive attempts to access a disk.</span></span> <span data-ttu-id="a3160-106">然後，系統管理員可以使用事件記錄檔來協助判斷哪些狀況造成錯誤，並找出發生錯誤的內容。</span><span class="sxs-lookup"><span data-stu-id="a3160-106">The system administrator can then use the event log to help determine what conditions caused the error and identify the context in which it occurred.</span></span> <span data-ttu-id="a3160-107">藉由定期查看事件記錄檔，系統管理員可以找出問題 (例如失敗的硬碟) ，然後才會造成損毀。</span><span class="sxs-lookup"><span data-stu-id="a3160-107">By periodically viewing the event log, the system administrator may be able to identify problems (such as a failing hard disk) before they cause damage.</span></span>

> [!Note]  
> <span data-ttu-id="a3160-108">事件記錄 API 是針對在 Windows Server 2003、Windows XP 或 Windows 2000 作業系統上執行的應用程式所設計。</span><span class="sxs-lookup"><span data-stu-id="a3160-108">The Event Logging API was designed for applications that run on the Windows Server 2003, Windows XP, or Windows 2000 operating system.</span></span> <span data-ttu-id="a3160-109">在 Windows Vista 中，已重新設計事件記錄基礎結構。</span><span class="sxs-lookup"><span data-stu-id="a3160-109">In Windows Vista, the event logging infrastructure was redesigned.</span></span> <span data-ttu-id="a3160-110">設計成在 Windows Vista 或更新版本的作業系統上執行的應用程式，現在應該會使用 [Windows 事件記錄](/windows/desktop/WES/windows-event-log) 檔來記錄事件。</span><span class="sxs-lookup"><span data-stu-id="a3160-110">Applications that are designed to run on the Windows Vista or later operating systems should now use [Windows Event Log](/windows/desktop/WES/windows-event-log) to log events.</span></span>

 
<span data-ttu-id="a3160-111">本節討論使用事件記錄撰寫和取用事件的程式設計介面。</span><span class="sxs-lookup"><span data-stu-id="a3160-111">This section discusses the programming interface for writing and consuming events using Event Logging.</span></span>

-   [<span data-ttu-id="a3160-112">事件類型</span><span class="sxs-lookup"><span data-stu-id="a3160-112">Event types</span></span>](event-types.md)
-   [<span data-ttu-id="a3160-113">記錄指導方針</span><span class="sxs-lookup"><span data-stu-id="a3160-113">Logging guidelines</span></span>](logging-guidelines.md)
-   [<span data-ttu-id="a3160-114">事件記錄元素</span><span class="sxs-lookup"><span data-stu-id="a3160-114">Event logging elements</span></span>](event-logging-elements.md)
-   [<span data-ttu-id="a3160-115">事件記錄作業</span><span class="sxs-lookup"><span data-stu-id="a3160-115">Event logging operations</span></span>](event-logging-operations.md)
-   [<span data-ttu-id="a3160-116">事件記錄模型</span><span class="sxs-lookup"><span data-stu-id="a3160-116">Event logging model</span></span>](event-logging-model.md)
-   [<span data-ttu-id="a3160-117">事件記錄安全性</span><span class="sxs-lookup"><span data-stu-id="a3160-117">Event logging security</span></span>](event-logging-security.md)

> [!Note]  
> <span data-ttu-id="a3160-118">在 Windows Server 2003、Windows XP 或 Windows 2000 電腦上發佈大於 64 kb 之事件的應用程式，將無法在 Windows Vista 或更新版本的電腦上發佈事件。</span><span class="sxs-lookup"><span data-stu-id="a3160-118">Applications that publish events that are larger than 64 kilobytes on a Windows Server 2003, Windows XP, or Windows 2000 computer will not be able to publish events on a Windows Vista or later computer.</span></span>
