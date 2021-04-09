---
title: Microsoft 代理程式設計介面總覽
description: Microsoft 代理程式設計介面總覽
ms.assetid: 8709441b-9739-4f11-a2de-40a5f5eefb72
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad89249e064eb89d37f497fb79cb8982c79cb83c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840099"
---
# <a name="microsoft-agent-programming-interface-overview"></a><span data-ttu-id="931e2-103">Microsoft 代理程式設計介面總覽</span><span class="sxs-lookup"><span data-stu-id="931e2-103">Microsoft Agent Programming Interface Overview</span></span>

<span data-ttu-id="931e2-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="931e2-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="931e2-105">Microsoft Agent API 提供支援動畫字元之顯示和動畫的服務。</span><span class="sxs-lookup"><span data-stu-id="931e2-105">The Microsoft Agent API provides services that support the display and animation of animated characters.</span></span> <span data-ttu-id="931e2-106">Microsoft Agent 會實作為 OLE Automation (元件物件模型 \[ COM \]) server，可讓多個應用程式（稱為用戶端或用戶端應用程式）同時裝載和存取其動畫、輸入和輸出服務。</span><span class="sxs-lookup"><span data-stu-id="931e2-106">Implemented as an OLE Automation (Component Object Model \[COM\]) server, Microsoft Agent enables multiple applications, called clients or client applications, to host and access its animation, input, and output services at the same time.</span></span> <span data-ttu-id="931e2-107">用戶端可以是連接至 Microsoft 代理程式 COM 介面的任何應用程式。</span><span class="sxs-lookup"><span data-stu-id="931e2-107">A client can be any application that connects to the Microsoft Agent's COM interfaces.</span></span>

<span data-ttu-id="931e2-108">作為 COM 伺服器，只有在用戶端應用程式使用 COM 介面和要求連接到該伺服器時，Microsoft Agent 才會自動啟動。</span><span class="sxs-lookup"><span data-stu-id="931e2-108">As a COM server, Microsoft Agent automatically starts up only when a client application uses the COM interfaces and requests to connect to it.</span></span> <span data-ttu-id="931e2-109">它會繼續執行，直到所有用戶端關閉其連接為止。</span><span class="sxs-lookup"><span data-stu-id="931e2-109">It remains running until all clients close their connections.</span></span> <span data-ttu-id="931e2-110">如果沒有連線的用戶端，Microsoft 代理程式會自動結束。</span><span class="sxs-lookup"><span data-stu-id="931e2-110">When no connected clients remain, Microsoft Agent automatically exits.</span></span>

<span data-ttu-id="931e2-111">雖然您可以直接呼叫 Microsoft 代理程式的 COM 介面，但 Microsoft 代理程式也包含 Microsoft ActiveX 控制項。</span><span class="sxs-lookup"><span data-stu-id="931e2-111">Although you can call Microsoft Agent's COM interfaces directly, Microsoft Agent also includes a Microsoft ActiveX control.</span></span> <span data-ttu-id="931e2-112">此控制項可讓您輕鬆地從支援 ActiveX 控制項介面的程式設計語言存取 Microsoft 代理程式的服務。</span><span class="sxs-lookup"><span data-stu-id="931e2-112">This control makes it easy to access Microsoft Agent's services from programming languages that support the ActiveX control interface.</span></span>

<span data-ttu-id="931e2-113">除了支援針對 Windows 撰寫的獨立程式之外，您還可以編寫代理程式支援網頁的腳本，但前提是瀏覽器支援 ActiveX 介面。</span><span class="sxs-lookup"><span data-stu-id="931e2-113">In addition to supporting stand-alone programs written for Windows, Agent can be scripted to support webpages, provided that the browser supports the ActiveX interface.</span></span> <span data-ttu-id="931e2-114">Microsoft Internet Explorer 包含 ActiveX 和指令碼語言的支援，可讓您用來設計代理程式。</span><span class="sxs-lookup"><span data-stu-id="931e2-114">Microsoft Internet Explorer includes support for ActiveX as well as scripting languages that you can use to program Agent.</span></span> <span data-ttu-id="931e2-115">如果您不是使用 Internet Explorer，請洽詢您的廠商或供應商，以瞭解瀏覽器對 ActiveX 的支援。</span><span class="sxs-lookup"><span data-stu-id="931e2-115">If you are not using Internet Explorer, consult with your vendor or supplier about the browser's support for ActiveX.</span></span>

<span data-ttu-id="931e2-116">下列資訊提供 Microsoft 代理程式軟體之程式設計介面的簡短總覽。</span><span class="sxs-lookup"><span data-stu-id="931e2-116">The following information provides a brief overview of the programming interfaces for the Microsoft Agent software.</span></span>

-   [<span data-ttu-id="931e2-117">動畫服務</span><span class="sxs-lookup"><span data-stu-id="931e2-117">Animation Services</span></span>](animation-services.md)
-   [<span data-ttu-id="931e2-118">輸入服務</span><span class="sxs-lookup"><span data-stu-id="931e2-118">Input Services</span></span>](input-services.md)
-   [<span data-ttu-id="931e2-119">語音命令視窗</span><span class="sxs-lookup"><span data-stu-id="931e2-119">The Voice Commands Window</span></span>](the-voice-commands-window.md)
-   [<span data-ttu-id="931e2-120">輸出服務</span><span class="sxs-lookup"><span data-stu-id="931e2-120">Output Services</span></span>](output-services.md)

 

 




