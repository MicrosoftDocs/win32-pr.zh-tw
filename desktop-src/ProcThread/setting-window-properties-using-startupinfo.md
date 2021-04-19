---
description: 父進程可以指定與其子進程主視窗相關聯的屬性。
ms.assetid: 12547da4-8d41-48c5-8efc-f0423f64caa7
title: 使用 STARTUPINFO 設定視窗屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ff59f9ae4473174325880a863f5b1f2fc4203e7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106977048"
---
# <a name="setting-window-properties-using-startupinfo"></a><span data-ttu-id="49b34-103">使用 STARTUPINFO 設定視窗屬性</span><span class="sxs-lookup"><span data-stu-id="49b34-103">Setting Window Properties Using STARTUPINFO</span></span>

<span data-ttu-id="49b34-104">父進程可以指定與其子進程主視窗相關聯的屬性。</span><span class="sxs-lookup"><span data-stu-id="49b34-104">A parent process can specify properties associated with the main window of its child process.</span></span> <span data-ttu-id="49b34-105">[**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa)函式會採用 [**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa)結構的指標作為其參數的其中一個。</span><span class="sxs-lookup"><span data-stu-id="49b34-105">The [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) function takes a pointer to a [**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa) structure as one of its parameters.</span></span> <span data-ttu-id="49b34-106">您可以使用此結構的成員來指定子進程主視窗的特性。</span><span class="sxs-lookup"><span data-stu-id="49b34-106">Use the members of this structure to specify characteristics of the child process's main window.</span></span> <span data-ttu-id="49b34-107">**DwFlags** 成員包含一個位，可決定要使用結構的其他成員。</span><span class="sxs-lookup"><span data-stu-id="49b34-107">The **dwFlags** member contains a bitfield that determines which other members of the structure are used.</span></span> <span data-ttu-id="49b34-108">這可讓您指定視窗屬性之任何子集的值。</span><span class="sxs-lookup"><span data-stu-id="49b34-108">This allows you to specify values for any subset of the window properties.</span></span> <span data-ttu-id="49b34-109">系統會針對您未指定的屬性使用預設值。</span><span class="sxs-lookup"><span data-stu-id="49b34-109">The system uses default values for the properties you do not specify.</span></span> <span data-ttu-id="49b34-110">**DwFlags** 成員也可以在初始化新的進程期間，強制顯示意見反應資料指標。</span><span class="sxs-lookup"><span data-stu-id="49b34-110">The **dwFlags** member can also force a feedback cursor to be displayed during the initialization of the new process.</span></span>

<span data-ttu-id="49b34-111">若是 GUI 進程， [**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa) 結構會指定當新的進程第一次呼叫 [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) 和 [**ShowWindow**](/windows/win32/api/winuser/nf-winuser-showwindow) 函式來建立和顯示重迭的視窗時，所要使用的預設值。</span><span class="sxs-lookup"><span data-stu-id="49b34-111">For GUI processes, the [**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa) structure specifies the default values to be used the first time the new process calls the [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) and [**ShowWindow**](/windows/win32/api/winuser/nf-winuser-showwindow) functions to create and display an overlapped window.</span></span> <span data-ttu-id="49b34-112">您可以指定下列預設值：</span><span class="sxs-lookup"><span data-stu-id="49b34-112">The following default values can be specified:</span></span>

-   <span data-ttu-id="49b34-113">由 [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa)建立之視窗的寬度和高度（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="49b34-113">The width and height, in pixels, of the window created by [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa).</span></span>
-   <span data-ttu-id="49b34-114">由 [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa)建立的視窗在螢幕座標中的位置。</span><span class="sxs-lookup"><span data-stu-id="49b34-114">The location, in screen coordinates of the window created by [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa).</span></span>
-   <span data-ttu-id="49b34-115">[**ShowWindow**](/windows/win32/api/winuser/nf-winuser-showwindow)的 *nCmdShow* 參數。</span><span class="sxs-lookup"><span data-stu-id="49b34-115">The *nCmdShow* parameter of [**ShowWindow**](/windows/win32/api/winuser/nf-winuser-showwindow).</span></span>

<span data-ttu-id="49b34-116">若為主控台進程，請在建立新主控台時使用 [**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa) 結構來指定視窗屬性 (使用 [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) 搭配 CREATE \_ new \_ console 或 [**AllocConsole**](/windows/console/allocconsole) 函數) 。</span><span class="sxs-lookup"><span data-stu-id="49b34-116">For console processes, use the [**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa) structure to specify window properties only when creating a new console (either using [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) with CREATE\_NEW\_CONSOLE or with the [**AllocConsole**](/windows/console/allocconsole) function).</span></span> <span data-ttu-id="49b34-117">**STARTUPINFO** 結構可以用來指定下列主控台視窗屬性：</span><span class="sxs-lookup"><span data-stu-id="49b34-117">The **STARTUPINFO** structure can be used to specify the following console window properties:</span></span>

-   <span data-ttu-id="49b34-118">新主控台視窗的大小（以字元儲存格為限）。</span><span class="sxs-lookup"><span data-stu-id="49b34-118">The size of the new console window, in character cells.</span></span>
-   <span data-ttu-id="49b34-119">新主控台視窗的位置（以螢幕座標為單位）。</span><span class="sxs-lookup"><span data-stu-id="49b34-119">The location of the new console window, in screen coordinates.</span></span>
-   <span data-ttu-id="49b34-120">新主控台螢幕緩衝區的大小（以字元資料格為限）。</span><span class="sxs-lookup"><span data-stu-id="49b34-120">The size, in character cells, of the new console's screen buffer.</span></span>
-   <span data-ttu-id="49b34-121">新主控台螢幕緩衝區的文字和背景色彩屬性。</span><span class="sxs-lookup"><span data-stu-id="49b34-121">The text and background color attributes of the new console's screen buffer.</span></span>
-   <span data-ttu-id="49b34-122">新主控台視窗的標題。</span><span class="sxs-lookup"><span data-stu-id="49b34-122">The title of the new console's window.</span></span>

 

 
