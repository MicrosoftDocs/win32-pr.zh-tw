---
title: 移植 X 視窗系統應用程式
description: 移植 X 視窗系統應用程式
ms.assetid: 730602f3-12af-430d-a105-0efdd3fd43b4
keywords:
- Windows 上的 OpenGL，移植
- 移植至 OpenGL、X 視窗系統
- OpenGL 移植 X 視窗系統
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b9e52a06ffa458e07a70a7c4823e0291639d878
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104183602"
---
# <a name="porting-x-window-system-applications"></a><span data-ttu-id="4ffaf-106">移植 X 視窗系統應用程式</span><span class="sxs-lookup"><span data-stu-id="4ffaf-106">Porting X Window System Applications</span></span>

<span data-ttu-id="4ffaf-107">就像 Windows 一樣，X 視窗系統是事件處理、以訊息為基礎的系統，使用視窗控制項和功能表。</span><span class="sxs-lookup"><span data-stu-id="4ffaf-107">Like Windows, the X Window System is an event-handling, message-based system that uses window controls and menus.</span></span> <span data-ttu-id="4ffaf-108">您 X 視窗系統應用程式中的 OpenGL 程式碼可能位於與您將它移植到 Windows 時所顯示的位置大致對應的區域中。</span><span class="sxs-lookup"><span data-stu-id="4ffaf-108">The OpenGL code in your X Window System application is probably located in areas that roughly correspond to where it will appear when you port it to Windows.</span></span> <span data-ttu-id="4ffaf-109">大部分的 OpenGL 程式碼都不會變更，但是您必須重寫 X 視窗系統專屬的任何程式碼。</span><span class="sxs-lookup"><span data-stu-id="4ffaf-109">Most of your OpenGL code will not change, but you must rewrite any code that is specific to the X Window System.</span></span>

<span data-ttu-id="4ffaf-110">**使用下列一般程式，將您的 X Window 系統 OpenGL 程式移植到 Windows**</span><span class="sxs-lookup"><span data-stu-id="4ffaf-110">**Use the following general procedure to port your X Window System OpenGL programs to Windows**</span></span>

1.  <span data-ttu-id="4ffaf-111">使用對等的 Windows 程式碼重寫 X 視窗系統特定的程式碼。</span><span class="sxs-lookup"><span data-stu-id="4ffaf-111">Rewrite the X Window System specific code using equivalent Windows code.</span></span> <span data-ttu-id="4ffaf-112">找出視窗建立和事件處理常式代碼。</span><span class="sxs-lookup"><span data-stu-id="4ffaf-112">Locate window-creation and event-handling code.</span></span> <span data-ttu-id="4ffaf-113">X 視窗系統和視窗是事件處理、訊息型的視窗化系統，可讓您更輕鬆地判斷要在哪裡進行適當的變更。</span><span class="sxs-lookup"><span data-stu-id="4ffaf-113">The X Window System and Windows are event-handling, message-based windowing systems, which makes it easier to determine where to make the appropriate changes.</span></span> <span data-ttu-id="4ffaf-114"> (不過，特別是對於大型應用程式，將應用程式從一個作業系統重寫為另一個作業系統可能是複雜且困難的工作。 ) </span><span class="sxs-lookup"><span data-stu-id="4ffaf-114">(However, especially for large applications, rewriting an application from one operating system to another can be a complex and difficult undertaking.)</span></span>
2.  <span data-ttu-id="4ffaf-115">找出使用 GLX 函數的任何程式碼。</span><span class="sxs-lookup"><span data-stu-id="4ffaf-115">Locate any code that uses GLX functions.</span></span> <span data-ttu-id="4ffaf-116">這些是您將轉譯為其對等 Windows 函式的函式。</span><span class="sxs-lookup"><span data-stu-id="4ffaf-116">These are the functions you'll translate to their equivalent Windows functions.</span></span>
3.  <span data-ttu-id="4ffaf-117">將 GLX 像素格式函式和視覺化/可繪製函數轉譯為適當的 Windows/OpenGL 像素格式和裝置內容函式。</span><span class="sxs-lookup"><span data-stu-id="4ffaf-117">Translate GLX pixel format functions and Visual/Drawable functions to appropriate Windows/OpenGL pixel format and device context functions.</span></span>
4.  <span data-ttu-id="4ffaf-118">將 GLX 轉譯內容函式轉譯為 Windows/OpenGL 轉譯內容函數。</span><span class="sxs-lookup"><span data-stu-id="4ffaf-118">Translate GLX rendering context functions to Windows/OpenGL rendering context functions.</span></span>
5.  <span data-ttu-id="4ffaf-119">將 GLX Pixmap 函數轉譯為對等的 Windows 函式。</span><span class="sxs-lookup"><span data-stu-id="4ffaf-119">Translate GLX Pixmap functions to equivalent Windows functions.</span></span>
6.  <span data-ttu-id="4ffaf-120">將 GLX 畫面格緩衝區和其他 GLX 函數轉譯為適當的 Windows 函式。</span><span class="sxs-lookup"><span data-stu-id="4ffaf-120">Translate GLX framebuffer and other GLX functions to the appropriate Windows functions.</span></span>

 

 




