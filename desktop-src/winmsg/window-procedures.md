---
description: 本節討論視窗程式。 每個視窗都有相關聯的視窗程式，可處理所有傳送或張貼至類別之視窗的訊息。
ms.assetid: vs|winui|~\winui\windowsuserinterface\windowing\windowprocedures.htm
title: 視窗程式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92ae68ba9b64557a6dc70d5c83788b8337648a2f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106988996"
---
# <a name="window-procedures"></a><span data-ttu-id="99a67-104">視窗程式</span><span class="sxs-lookup"><span data-stu-id="99a67-104">Window Procedures</span></span>

<span data-ttu-id="99a67-105">每個視窗都有相關聯的視窗程式，這個函式會處理所有傳送或張貼至類別之視窗的訊息。</span><span class="sxs-lookup"><span data-stu-id="99a67-105">Every window has an associated window procedure — a function that processes all messages sent or posted to all windows of the class.</span></span> <span data-ttu-id="99a67-106">視窗外觀和行為的所有層面都取決於視窗程式對這些訊息的回應。</span><span class="sxs-lookup"><span data-stu-id="99a67-106">All aspects of a window's appearance and behavior depend on the window procedure's response to these messages.</span></span>

### <a name="in-this-section"></a><span data-ttu-id="99a67-107">本節內容</span><span class="sxs-lookup"><span data-stu-id="99a67-107">In This Section</span></span>



| <span data-ttu-id="99a67-108">Name</span><span class="sxs-lookup"><span data-stu-id="99a67-108">Name</span></span>                                                         | <span data-ttu-id="99a67-109">描述</span><span class="sxs-lookup"><span data-stu-id="99a67-109">Description</span></span>                                                                                                                                                                                                    |
|--------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="99a67-110">關於視窗程式</span><span class="sxs-lookup"><span data-stu-id="99a67-110">About Window Procedures</span></span>](about-window-procedures.md)       | <span data-ttu-id="99a67-111">討論視窗程式。</span><span class="sxs-lookup"><span data-stu-id="99a67-111">Discusses window procedures.</span></span> <span data-ttu-id="99a67-112">每個視窗都是特定視窗類別的成員。</span><span class="sxs-lookup"><span data-stu-id="99a67-112">Each window is a member of a particular window class.</span></span> <span data-ttu-id="99a67-113">視窗類別會決定個別視窗用來處理其訊息的預設視窗程式。</span><span class="sxs-lookup"><span data-stu-id="99a67-113">The window class determines the default window procedure that an individual window uses to process its messages.</span></span><br/> |
| [<span data-ttu-id="99a67-114">使用視窗程式</span><span class="sxs-lookup"><span data-stu-id="99a67-114">Using Window Procedures</span></span>](using-window-procedures.md)       | <span data-ttu-id="99a67-115">涵蓋如何執行與視窗程式相關聯的下列工作。</span><span class="sxs-lookup"><span data-stu-id="99a67-115">Covers how to perform the following tasks associated with window procedures.</span></span><br/>                                                                                                                        |
| [<span data-ttu-id="99a67-116">視窗程式參考</span><span class="sxs-lookup"><span data-stu-id="99a67-116">Window Procedure Reference</span></span>](window-procedure-reference.md) | <span data-ttu-id="99a67-117">包含 API 參考。</span><span class="sxs-lookup"><span data-stu-id="99a67-117">Contains the API reference.</span></span><br/>                                                                                                                                                                         |



 

### <a name="functions"></a><span data-ttu-id="99a67-118">函式</span><span class="sxs-lookup"><span data-stu-id="99a67-118">Functions</span></span>



| <span data-ttu-id="99a67-119">Name</span><span class="sxs-lookup"><span data-stu-id="99a67-119">Name</span></span>                                     | <span data-ttu-id="99a67-120">描述</span><span class="sxs-lookup"><span data-stu-id="99a67-120">Description</span></span>                                                                                                                                                                                                                                                                                                   |
|------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="99a67-121">**CallWindowProc**</span><span class="sxs-lookup"><span data-stu-id="99a67-121">**CallWindowProc**</span></span>](/windows/win32/api/winuser/nf-winuser-callwindowproca) | <span data-ttu-id="99a67-122">將訊息資訊傳遞給指定的視窗程式。</span><span class="sxs-lookup"><span data-stu-id="99a67-122">Passes message information to the specified window procedure.</span></span> <br/>                                                                                                                                                                                                                                     |
| [<span data-ttu-id="99a67-123">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="99a67-123">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)   | <span data-ttu-id="99a67-124">呼叫預設視窗程式，為應用程式未處理的任何視窗訊息提供預設處理。</span><span class="sxs-lookup"><span data-stu-id="99a67-124">Calls the default window procedure to provide default processing for any window messages that an application does not process.</span></span> <span data-ttu-id="99a67-125">這個函式可確保處理每個訊息。</span><span class="sxs-lookup"><span data-stu-id="99a67-125">This function ensures that every message is processed.</span></span> <span data-ttu-id="99a67-126">呼叫 [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)時所使用的參數，與視窗程式所收到的參數相同。</span><span class="sxs-lookup"><span data-stu-id="99a67-126">[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) is called with the same parameters received by the window procedure.</span></span> <br/> |
| <span data-ttu-id="99a67-127">[*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="99a67-127">[*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))</span></span>           | <span data-ttu-id="99a67-128">處理傳送至視窗之訊息的應用程式定義函數。</span><span class="sxs-lookup"><span data-stu-id="99a67-128">An application-defined function that processes messages sent to a window.</span></span> <span data-ttu-id="99a67-129">**WNDPROC** 型別定義此回呼函數的指標。</span><span class="sxs-lookup"><span data-stu-id="99a67-129">The **WNDPROC** type defines a pointer to this callback function.</span></span> <span data-ttu-id="99a67-130">[*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) 是應用程式定義函數名稱的預留位置。</span><span class="sxs-lookup"><span data-stu-id="99a67-130">[*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) is a placeholder for the application-defined function name.</span></span> <br/>                                                            |



 

 

 
