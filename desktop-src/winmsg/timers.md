---
description: 本主題討論計時器。 計時器是一種內部常式，可重複測量指定的間隔（以毫秒為單位）。
ms.assetid: vs|winui|~\winui\windowsuserinterface\windowing\timers.htm
title: 計時器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5fa44be05acc09eafed550a200ed6bc61f79daa2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106994540"
---
# <a name="timers"></a><span data-ttu-id="ce58b-104">計時器</span><span class="sxs-lookup"><span data-stu-id="ce58b-104">Timers</span></span>

<span data-ttu-id="ce58b-105">計時器是一種內部常式，可重複測量指定的間隔（以毫秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="ce58b-105">A timer is an internal routine that repeatedly measures a specified interval, in milliseconds.</span></span>

### <a name="in-this-section"></a><span data-ttu-id="ce58b-106">本節內容</span><span class="sxs-lookup"><span data-stu-id="ce58b-106">In This Section</span></span>



| <span data-ttu-id="ce58b-107">Name</span><span class="sxs-lookup"><span data-stu-id="ce58b-107">Name</span></span>                                   | <span data-ttu-id="ce58b-108">描述</span><span class="sxs-lookup"><span data-stu-id="ce58b-108">Description</span></span>                                                                                                               |
|----------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ce58b-109">關於計時器</span><span class="sxs-lookup"><span data-stu-id="ce58b-109">About Timers</span></span>](about-timers.md)       | <span data-ttu-id="ce58b-110">描述如何建立、識別、設定和刪除計時器。</span><span class="sxs-lookup"><span data-stu-id="ce58b-110">Describes how to create, identify, set, and delete timers.</span></span><br/>                                                     |
| [<span data-ttu-id="ce58b-111">使用計時器</span><span class="sxs-lookup"><span data-stu-id="ce58b-111">Using Timers</span></span>](using-timers.md)       | <span data-ttu-id="ce58b-112">討論如何建立和終結計時器，以及如何使用計時器以指定的間隔來陷印滑鼠輸入。</span><span class="sxs-lookup"><span data-stu-id="ce58b-112">Discusses how to create and destroy timers, and how to use a timer to trap mouse input at specified intervals.</span></span><br/> |
| [<span data-ttu-id="ce58b-113">計時器參考</span><span class="sxs-lookup"><span data-stu-id="ce58b-113">Timer Reference</span></span>](timer-reference.md) | <span data-ttu-id="ce58b-114">包含 API 參考。</span><span class="sxs-lookup"><span data-stu-id="ce58b-114">Contains the API reference.</span></span><br/>                                                                                    |



 

### <a name="timer-functions"></a><span data-ttu-id="ce58b-115">Timer 函數</span><span class="sxs-lookup"><span data-stu-id="ce58b-115">Timer Functions</span></span>



| <span data-ttu-id="ce58b-116">Name</span><span class="sxs-lookup"><span data-stu-id="ce58b-116">Name</span></span>                           | <span data-ttu-id="ce58b-117">描述</span><span class="sxs-lookup"><span data-stu-id="ce58b-117">Description</span></span>                                                                                                                                                                                                                                                              |
|--------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ce58b-118">**KillTimer**</span><span class="sxs-lookup"><span data-stu-id="ce58b-118">**KillTimer**</span></span>](/windows/win32/api/winuser/nf-winuser-killtimer) | <span data-ttu-id="ce58b-119">終結指定的計時器。</span><span class="sxs-lookup"><span data-stu-id="ce58b-119">Destroys the specified timer.</span></span> <br/>                                                                                                                                                                                                                                |
| [<span data-ttu-id="ce58b-120">**SetTimer**</span><span class="sxs-lookup"><span data-stu-id="ce58b-120">**SetTimer**</span></span>](/windows/win32/api/winuser/nf-winuser-settimer)   | <span data-ttu-id="ce58b-121">使用指定的超時時間值建立計時器。</span><span class="sxs-lookup"><span data-stu-id="ce58b-121">Creates a timer with the specified time-out value.</span></span><br/>                                                                                                                                                                                                            |
| [<span data-ttu-id="ce58b-122">*TimerProc*</span><span class="sxs-lookup"><span data-stu-id="ce58b-122">*TimerProc*</span></span>](/windows/win32/api/winuser/nc-winuser-timerproc)   | <span data-ttu-id="ce58b-123">處理 [**WM \_ 計時器**](wm-timer.md) 訊息的應用程式定義回呼函數。</span><span class="sxs-lookup"><span data-stu-id="ce58b-123">An application-defined callback function that processes [**WM\_TIMER**](wm-timer.md) messages.</span></span> <span data-ttu-id="ce58b-124">**TIMERPROC** 型別定義此回呼函數的指標。</span><span class="sxs-lookup"><span data-stu-id="ce58b-124">The **TIMERPROC** type defines a pointer to this callback function.</span></span> <span data-ttu-id="ce58b-125">[*TimerProc*](/windows/win32/api/winuser/nc-winuser-timerproc) 是應用程式定義函數名稱的預留位置。</span><span class="sxs-lookup"><span data-stu-id="ce58b-125">[*TimerProc*](/windows/win32/api/winuser/nc-winuser-timerproc) is a placeholder for the application-defined function name.</span></span> <br/> |



 

### <a name="timer-notifications"></a><span data-ttu-id="ce58b-126">計時器通知</span><span class="sxs-lookup"><span data-stu-id="ce58b-126">Timer Notifications</span></span>



| <span data-ttu-id="ce58b-127">Name</span><span class="sxs-lookup"><span data-stu-id="ce58b-127">Name</span></span>                          | <span data-ttu-id="ce58b-128">描述</span><span class="sxs-lookup"><span data-stu-id="ce58b-128">Description</span></span>                                                                                                                                                                                     |
|-------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ce58b-129">**WM \_ 計時器**</span><span class="sxs-lookup"><span data-stu-id="ce58b-129">**WM\_TIMER**</span></span>](wm-timer.md) | <span data-ttu-id="ce58b-130">當計時器到期時，張貼至安裝執行緒的訊息佇列。</span><span class="sxs-lookup"><span data-stu-id="ce58b-130">Posted to the installing thread's message queue when a timer expires.</span></span> <span data-ttu-id="ce58b-131">此訊息是由 [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) 或 [**PeekMessage**](/windows/win32/api/winuser/nf-winuser-peekmessagea) 函數所張貼。</span><span class="sxs-lookup"><span data-stu-id="ce58b-131">The message is posted by the [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) or [**PeekMessage**](/windows/win32/api/winuser/nf-winuser-peekmessagea) function.</span></span> <br/> |



 

 

 
