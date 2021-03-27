---
description: 事件追蹤會話會記錄一或多個提供者的事件。
ms.assetid: 43841d2f-5a4c-493d-9531-21941311ffbc
title: 控制事件追蹤會話
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b03f1917354679e7a68f9dbd001fc3aa10f09db0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972232"
---
# <a name="controlling-event-tracing-sessions"></a><span data-ttu-id="afb78-103">控制事件追蹤會話</span><span class="sxs-lookup"><span data-stu-id="afb78-103">Controlling Event Tracing Sessions</span></span>

<span data-ttu-id="afb78-104">事件追蹤會話會記錄一或多個 [提供者](providing-events.md)的事件。</span><span class="sxs-lookup"><span data-stu-id="afb78-104">Event tracing sessions record events from one or more [providers](providing-events.md).</span></span> <span data-ttu-id="afb78-105">控制器會定義會話並啟用提供者。</span><span class="sxs-lookup"><span data-stu-id="afb78-105">The controller defines the session and enables the providers.</span></span> <span data-ttu-id="afb78-106">定義會話通常包括指定會話和記錄檔名稱、要使用的記錄檔類型，以及用來記錄事件的時間戳記解析。</span><span class="sxs-lookup"><span data-stu-id="afb78-106">Defining the session typically includes specifying the session and log file name, type of log file to use, and the resolution of the time stamp used to record the events.</span></span> <span data-ttu-id="afb78-107">控制器也可以更新和查詢事件追蹤會話。</span><span class="sxs-lookup"><span data-stu-id="afb78-107">Controllers can also update and query event tracing sessions.</span></span>

<span data-ttu-id="afb78-108">下列主題將示範如何定義和更新會話，以及如何啟用事件追蹤提供者：</span><span class="sxs-lookup"><span data-stu-id="afb78-108">The following topics demonstrate how to define and update a session, and enable event trace providers:</span></span>

-   [<span data-ttu-id="afb78-109">設定和啟動事件追蹤會話</span><span class="sxs-lookup"><span data-stu-id="afb78-109">Configuring and Starting an Event Tracing Session</span></span>](configuring-and-starting-an-event-tracing-session.md)
-   [<span data-ttu-id="afb78-110">設定並啟動 SystemTraceProvider 會話</span><span class="sxs-lookup"><span data-stu-id="afb78-110">Configuring and Starting a SystemTraceProvider Session</span></span>](configuring-and-starting-a-systemtraceprovider-session.md)
-   [<span data-ttu-id="afb78-111">設定和啟動自動記錄器會話</span><span class="sxs-lookup"><span data-stu-id="afb78-111">Configuring and Starting an AutoLogger Session</span></span>](configuring-and-starting-an-autologger-session.md)
-   [<span data-ttu-id="afb78-112">設定和啟動私用記錄器會話</span><span class="sxs-lookup"><span data-stu-id="afb78-112">Configuring and Starting a Private Logger Session</span></span>](configuring-and-starting-a-private-logger-session.md)
-   [<span data-ttu-id="afb78-113">更新事件追蹤會話</span><span class="sxs-lookup"><span data-stu-id="afb78-113">Updating an Event Tracing Session</span></span>](updating-an-event-tracing-session.md)
-   [<span data-ttu-id="afb78-114">正在抓取其他事件追蹤資料</span><span class="sxs-lookup"><span data-stu-id="afb78-114">Retrieving Additional Event Tracing Data</span></span>](retrieving-additional-event-tracing-data.md)

<span data-ttu-id="afb78-115">如需排清和查詢會話的詳細資訊，請分別參閱 [**ControlTrace**](/windows/win32/api/evntrace/nf-evntrace-controltracea) 和 [**QueryAllTraces**](/windows/win32/api/evntrace/nf-evntrace-queryalltracesa)。</span><span class="sxs-lookup"><span data-stu-id="afb78-115">For information on flushing and querying sessions, see [**ControlTrace**](/windows/win32/api/evntrace/nf-evntrace-controltracea) and [**QueryAllTraces**](/windows/win32/api/evntrace/nf-evntrace-queryalltracesa), respectively.</span></span>

<span data-ttu-id="afb78-116">只有以較高的系統管理許可權執行的使用者、Performance Log Users 群組中的使用者，以及以 LocalSystem、LocalService 或 NetworkService 身分執行的應用程式，才能控制事件追蹤會話。</span><span class="sxs-lookup"><span data-stu-id="afb78-116">Only users running with elevated administrative privileges, users in the Performance Log Users group, and applications running as LocalSystem, LocalService or NetworkService can control event tracing sessions.</span></span> <span data-ttu-id="afb78-117">若要授與受限制的使用者控制追蹤會話的能力，請將它們新增至 Performance Log Users 群組。</span><span class="sxs-lookup"><span data-stu-id="afb78-117">To grant a restricted user the ability to control trace sessions, add them to the Performance Log Users group.</span></span>

<span data-ttu-id="afb78-118">**WINDOWS XP 和 windows 2000：** 任何人都可以控制追蹤會話。</span><span class="sxs-lookup"><span data-stu-id="afb78-118">**Windows XP and Windows 2000:** Anyone can control a trace session.</span></span>

 

 
