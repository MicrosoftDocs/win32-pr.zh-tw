---
title: Microsoft 代理程式伺服器介面程式設計
description: Microsoft 代理程式伺服器介面程式設計
ms.assetid: d1f9feb1-afcf-45a5-8ebf-7200c5963f70
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d9699a102884eeab5079e25aaa39fb6942c5f4ef
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104020703"
---
# <a name="programming-the-microsoft-agent-server-interface"></a><span data-ttu-id="4b0a9-103">Microsoft 代理程式伺服器介面程式設計</span><span class="sxs-lookup"><span data-stu-id="4b0a9-103">Programming the Microsoft Agent Server Interface</span></span>

<span data-ttu-id="4b0a9-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="4b0a9-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="4b0a9-105">Microsoft Agent 提供的服務可讓您從應用程式撰寫動畫的字元。</span><span class="sxs-lookup"><span data-stu-id="4b0a9-105">Microsoft Agent provides services that enable you to program animated characters from an application.</span></span> <span data-ttu-id="4b0a9-106">這些服務會實作為 OLE Automation 伺服器。</span><span class="sxs-lookup"><span data-stu-id="4b0a9-106">These services are implemented as an OLE Automation server.</span></span> <span data-ttu-id="4b0a9-107">OLE Automation 可讓應用程式以程式設計方式控制另一個應用程式的物件。</span><span class="sxs-lookup"><span data-stu-id="4b0a9-107">OLE Automation enables an application to control another application's object programmatically.</span></span> <span data-ttu-id="4b0a9-108">本檔假設您已瞭解元件物件模型 (COM) 和 OLE。</span><span class="sxs-lookup"><span data-stu-id="4b0a9-108">This document assumes an understanding of the Component Object Model (COM) and OLE.</span></span> <span data-ttu-id="4b0a9-109">如需這些服務的簡介，請參閱程式 [設計介面總覽](microsoft-agent-programming-interface-overview.md)。</span><span class="sxs-lookup"><span data-stu-id="4b0a9-109">For an introduction of these services, see the [Programming Interface Overview](microsoft-agent-programming-interface-overview.md).</span></span>

-   [<span data-ttu-id="4b0a9-110">將 Microsoft Agent 功能新增至您的應用程式</span><span class="sxs-lookup"><span data-stu-id="4b0a9-110">Adding Microsoft Agent Functionality to Your Application</span></span>](adding-microsoft-agent-functionality-to-your-application.md)
-   [<span data-ttu-id="4b0a9-111">載入字元和動畫資料</span><span class="sxs-lookup"><span data-stu-id="4b0a9-111">Loading Character and Animation Data</span></span>](loading-character-and-animation-data.md)
-   [<span data-ttu-id="4b0a9-112">建立通知接收</span><span class="sxs-lookup"><span data-stu-id="4b0a9-112">Creating a Notification Sink</span></span>](creating-a-notification-sink.md)
-   [<span data-ttu-id="4b0a9-113">使用 JAVA 存取服務</span><span class="sxs-lookup"><span data-stu-id="4b0a9-113">Accessing Services Using Java</span></span>](accessing-services-using-java.md)
-   [<span data-ttu-id="4b0a9-114">存取語音服務</span><span class="sxs-lookup"><span data-stu-id="4b0a9-114">Accessing Speech Services</span></span>](accessing-speech-services.md)
-   [<span data-ttu-id="4b0a9-115">參考</span><span class="sxs-lookup"><span data-stu-id="4b0a9-115">Reference</span></span>](reference.md)

 

 




