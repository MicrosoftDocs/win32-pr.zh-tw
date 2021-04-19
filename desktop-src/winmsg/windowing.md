---
description: 視窗化區段會描述應用程式的元素，其中包含以 Windows 為基礎的圖形化使用者介面。
ms.assetid: 2e00186d-cc1f-4954-a074-685efacb46de
title: Windows 和訊息
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed13b7507ba48a984d5eb1bb237794fb54434f01
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106975481"
---
# <a name="windows-and-messages"></a><span data-ttu-id="bedbc-103">Windows 和訊息</span><span class="sxs-lookup"><span data-stu-id="bedbc-103">Windows and Messages</span></span>

<span data-ttu-id="bedbc-104">下列各節描述具有 Windows 圖形使用者介面的應用程式元素。</span><span class="sxs-lookup"><span data-stu-id="bedbc-104">The following sections describe the elements of an application with a Windows-based graphical user interface.</span></span>

### <a name="in-this-section"></a><span data-ttu-id="bedbc-105">本節內容</span><span class="sxs-lookup"><span data-stu-id="bedbc-105">In This Section</span></span>



| <span data-ttu-id="bedbc-106">Name</span><span class="sxs-lookup"><span data-stu-id="bedbc-106">Name</span></span>                                                           | <span data-ttu-id="bedbc-107">描述</span><span class="sxs-lookup"><span data-stu-id="bedbc-107">Description</span></span>                                                                                                                                                                                                                  |
|----------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="bedbc-108">Windows</span><span class="sxs-lookup"><span data-stu-id="bedbc-108">Windows</span></span>](windows.md)                                         | <span data-ttu-id="bedbc-109">討論 windows 一般。</span><span class="sxs-lookup"><span data-stu-id="bedbc-109">Discusses windows in general.</span></span><br/>                                                                                                                                                                                     |
| [<span data-ttu-id="bedbc-110">視窗類別</span><span class="sxs-lookup"><span data-stu-id="bedbc-110">Window Classes</span></span>](window-classes.md)                           | <span data-ttu-id="bedbc-111">描述視窗類別的類型、系統如何找出它們，以及定義屬於它們之 windows 預設行為的元素。</span><span class="sxs-lookup"><span data-stu-id="bedbc-111">Describes the types of window classes, how the system locates them, and the elements that define the default behavior of windows that belong to them.</span></span><br/>                                                             |
| [<span data-ttu-id="bedbc-112">視窗程式</span><span class="sxs-lookup"><span data-stu-id="bedbc-112">Window Procedures</span></span>](window-procedures.md)                     | <span data-ttu-id="bedbc-113">討論視窗程式。</span><span class="sxs-lookup"><span data-stu-id="bedbc-113">Discusses window procedures.</span></span> <span data-ttu-id="bedbc-114">每個視窗都有相關聯的視窗程式，可處理所有傳送或張貼至類別之視窗的訊息。</span><span class="sxs-lookup"><span data-stu-id="bedbc-114">Every window has an associated window procedure that processes all messages sent or posted to all windows of the class.</span></span><br/>                                                              |
| [<span data-ttu-id="bedbc-115">訊息和訊息佇列</span><span class="sxs-lookup"><span data-stu-id="bedbc-115">Messages and Message Queues</span></span>](messages-and-message-queues.md) | <span data-ttu-id="bedbc-116">描述訊息和訊息佇列，以及如何在您的應用程式中使用它們。</span><span class="sxs-lookup"><span data-stu-id="bedbc-116">Describes messages and message queues and how to use them in your applications.</span></span><br/>                                                                                                                                   |
| [<span data-ttu-id="bedbc-117">計時器</span><span class="sxs-lookup"><span data-stu-id="bedbc-117">Timers</span></span>](timers.md)                                           | <span data-ttu-id="bedbc-118">討論計時器。</span><span class="sxs-lookup"><span data-stu-id="bedbc-118">Discusses timers.</span></span> <span data-ttu-id="bedbc-119">計時器是一種內部常式，可重複測量指定的間隔（以毫秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="bedbc-119">A timer is an internal routine that repeatedly measures a specified interval, in milliseconds.</span></span><br/>                                                                                                  |
| [<span data-ttu-id="bedbc-120">視窗屬性</span><span class="sxs-lookup"><span data-stu-id="bedbc-120">Window Properties</span></span>](window-properties.md)                     | <span data-ttu-id="bedbc-121">討論視窗屬性。</span><span class="sxs-lookup"><span data-stu-id="bedbc-121">Discusses window properties.</span></span> <span data-ttu-id="bedbc-122">視窗屬性是指派給視窗的任何資料。</span><span class="sxs-lookup"><span data-stu-id="bedbc-122">A window property is any data assigned to a window.</span></span><br/>                                                                                                                                  |
| [<span data-ttu-id="bedbc-123">Configuration</span><span class="sxs-lookup"><span data-stu-id="bedbc-123">Configuration</span></span>](configuration.md)                             | <span data-ttu-id="bedbc-124">描述可用來控制系統計量設定的函式，以及各種系統屬性，例如按兩下時間、螢幕保護裝置超時時間、視窗框線寬度和桌面圖案。</span><span class="sxs-lookup"><span data-stu-id="bedbc-124">Describes the functions that can be used to control the configuration of system metrics and various system attributes such as double-click time, screen saver time-out, window border width, and desktop pattern.</span></span><br/> |
| [<span data-ttu-id="bedbc-125">鉤</span><span class="sxs-lookup"><span data-stu-id="bedbc-125">Hooks</span></span>](hooks.md)                                             | <span data-ttu-id="bedbc-126">討論勾點。</span><span class="sxs-lookup"><span data-stu-id="bedbc-126">Discusses hooks.</span></span> <span data-ttu-id="bedbc-127">攔截是系統訊息處理機制中的一個點，可讓應用程式安裝副程式來監視訊息流量。</span><span class="sxs-lookup"><span data-stu-id="bedbc-127">A hook is a point in the system message-handling mechanism where an application can install a subroutine to monitor the message traffic.</span></span><br/>                                                         |
| [<span data-ttu-id="bedbc-128">多個檔介面</span><span class="sxs-lookup"><span data-stu-id="bedbc-128">Multiple Document Interface</span></span>](multiple-document-interface.md) | <span data-ttu-id="bedbc-129">討論多重檔介面，這是定義應用程式使用者介面的規格，可讓使用者同時使用多份檔。</span><span class="sxs-lookup"><span data-stu-id="bedbc-129">Discusses the Multiple Document Interface which is a specification that defines a user interface for applications that enable the user to work with more than one document at the same time.</span></span><br/>                      |



 

 

 




