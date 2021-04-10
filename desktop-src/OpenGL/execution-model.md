---
title: 執行模型
description: 執行模型
ms.assetid: 1947eb24-3a55-4d30-924e-93f2eed2c7b6
keywords:
- OpenGL、執行模型
- 執行模型 OpenGL
- OpenGL、用戶端/伺服器模型
- 用戶端/伺服器模型 OpenGL
- OpenGL、網路透明
- framebuffers，執行模型
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86012912f9bd963da0489b83cc4a5c1e7e1722ff
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103932475"
---
# <a name="execution-model"></a><span data-ttu-id="54e59-109">執行模型</span><span class="sxs-lookup"><span data-stu-id="54e59-109">Execution Model</span></span>

<span data-ttu-id="54e59-110">OpenGL 命令的解讀模型是用戶端/伺服器。</span><span class="sxs-lookup"><span data-stu-id="54e59-110">The model for interpretation of OpenGL commands is client/server.</span></span> <span data-ttu-id="54e59-111">應用程式程式碼 (用戶端) 發出命令，這些命令會由 OpenGL (伺服器) 進行解讀和處理。</span><span class="sxs-lookup"><span data-stu-id="54e59-111">Application code (the client) issues commands, which are interpreted and processed by OpenGL (the server).</span></span> <span data-ttu-id="54e59-112">伺服器不一定會與用戶端在同一部電腦上運作。</span><span class="sxs-lookup"><span data-stu-id="54e59-112">The server may or may not operate on the same computer as the client.</span></span> <span data-ttu-id="54e59-113">就這種情況而言，OpenGL 是網路透明的。</span><span class="sxs-lookup"><span data-stu-id="54e59-113">In this sense, OpenGL is network-transparent.</span></span> <span data-ttu-id="54e59-114">伺服器可以維護數個 OpenGL 內容，每個都是封裝的 OpenGL 狀態。</span><span class="sxs-lookup"><span data-stu-id="54e59-114">A server can maintain several OpenGL contexts, each of which is an encapsulated OpenGL state.</span></span> <span data-ttu-id="54e59-115">用戶端可以連接到這些內容的任何一個。</span><span class="sxs-lookup"><span data-stu-id="54e59-115">A client can connect to any one of these contexts.</span></span> <span data-ttu-id="54e59-116">您可以藉由擴充現有的通訊協定 (（例如 X 視窗系統) 或使用獨立的通訊協定）來執行必要的網路通訊協定。</span><span class="sxs-lookup"><span data-stu-id="54e59-116">The required network protocol can be implemented by augmenting an already existing protocol (such as that of the X Window System) or by using an independent protocol.</span></span> <span data-ttu-id="54e59-117">未提供任何 OpenGL 命令來取得使用者輸入。</span><span class="sxs-lookup"><span data-stu-id="54e59-117">No OpenGL commands are provided for obtaining user input.</span></span>

<span data-ttu-id="54e59-118">配置畫面格緩衝區資源的視窗系統最終會控制畫面格緩衝區上 OpenGL 命令的效果。</span><span class="sxs-lookup"><span data-stu-id="54e59-118">The window system that allocates framebuffer resources ultimately controls the effects of OpenGL commands on the framebuffer.</span></span> <span data-ttu-id="54e59-119">視窗系統：</span><span class="sxs-lookup"><span data-stu-id="54e59-119">The window system:</span></span>

-   <span data-ttu-id="54e59-120">判斷畫面格緩衝區 OpenGL 的哪些部分可在任何指定時間存取。</span><span class="sxs-lookup"><span data-stu-id="54e59-120">Determines which portions of the framebuffer OpenGL may access at any given time.</span></span>
-   <span data-ttu-id="54e59-121">將這些部分的結構傳達給 OpenGL。</span><span class="sxs-lookup"><span data-stu-id="54e59-121">Communicates to OpenGL how those portions are structured.</span></span>

<span data-ttu-id="54e59-122">因此，沒有可設定畫面格緩衝區或初始化 OpenGL 的 OpenGL 命令。</span><span class="sxs-lookup"><span data-stu-id="54e59-122">Therefore, there are no OpenGL commands to configure the framebuffer or initialize OpenGL.</span></span> <span data-ttu-id="54e59-123">框架緩衝區設定是在 OpenGL 之外與視窗系統一起完成;當視窗系統組態 OpenGL 轉譯的視窗時，就會發生 OpenGL 初始化。</span><span class="sxs-lookup"><span data-stu-id="54e59-123">Frame buffer configuration is done outside of OpenGL in conjunction with the window system; OpenGL initialization takes place when the window system allocates a window for OpenGL rendering.</span></span>

 

 




