---
description: 專家是 Microsoft Win32 動態連結程式庫 (DLL) ，可分析網路封包提供者 (NPP) 所收集的網路流量，並放入 capture 檔案中。
ms.assetid: 57d8164e-f587-4bb9-a0b1-6094037e584c
title: 專家
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bbf5fc0096b15d590bf70859443667f2d9969f1e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106971174"
---
# <a name="expert"></a><span data-ttu-id="3046d-103">專家</span><span class="sxs-lookup"><span data-stu-id="3046d-103">Expert</span></span>

<span data-ttu-id="3046d-104">專家是 Microsoft Win32 動態連結程式庫 (DLL) ，可分析 [*網路封包提供者*](n.md) (NPP) 所收集的網路流量，並放入 capture 檔案中。</span><span class="sxs-lookup"><span data-stu-id="3046d-104">An expert is a Microsoft Win32 dynamic-link library (DLL) that analyzes network traffic collected by a [*network packet provider*](n.md) (NPP), and placed in a capture file.</span></span> <span data-ttu-id="3046d-105">在資料被捕獲並儲存在 capture 檔案中之後，專家就可以使用剖析器（也稱為通訊協定剖析器）來分析檔案中的資料。</span><span class="sxs-lookup"><span data-stu-id="3046d-105">After the data is captured and stored in a capture file, the expert works with a parser, also referred to as a protocol parser, to analyze the data in the file.</span></span> <span data-ttu-id="3046d-106">例如，您可以檢查 capture 檔案的框架，並使用剖析 [*器來辨識通訊協定，例如*](p.md) 伺服器訊息區 (SMB) ，或傳輸控制通訊協定/網際網路通訊協定 (tcp/ip) 。</span><span class="sxs-lookup"><span data-stu-id="3046d-106">For example, you can examine the frames of the capture file and use a [*parser*](p.md) to recognize protocols such as server message block (SMB), or Transmission Control Protocol/Internet Protocol (TCP/IP).</span></span>

<span data-ttu-id="3046d-107">您可以設計專家來處理所有的網路監視器剖析器，以及您自行建立的任何剖析器。</span><span class="sxs-lookup"><span data-stu-id="3046d-107">You can design an expert to work with all of the Network Monitor parsers, and any parsers that you create yourself.</span></span>

<span data-ttu-id="3046d-108">當要求的通訊協定相符識別特定的畫面格之後，專家會將資料從框架中解壓縮。</span><span class="sxs-lookup"><span data-stu-id="3046d-108">After a requested match of protocols identifies a specific frame, the expert extracts data from the frame.</span></span> <span data-ttu-id="3046d-109">您可以設計專家來管理網路監視器事件檢視器所顯示之可用資料的資訊。</span><span class="sxs-lookup"><span data-stu-id="3046d-109">You can program the expert to manipulate information into usable data that the Network Monitor Event Viewer displays.</span></span>

<span data-ttu-id="3046d-110">您可以在執行時間設定專家，然後使用網路監視器儲存使用者設定資料，以使用不同的 capture 檔。</span><span class="sxs-lookup"><span data-stu-id="3046d-110">You can configure an expert at run time, and then use Network Monitor to save user configuration data for reuse with different capture files.</span></span> <span data-ttu-id="3046d-111">您可以使用專家為使用者提供相互關聯資料和自訂解決方案。</span><span class="sxs-lookup"><span data-stu-id="3046d-111">You can use an expert to provide correlation data and custom resolutions for end users.</span></span> <span data-ttu-id="3046d-112">如需有關建立 HTML 設定資訊的詳細資訊，請參閱 [事件參考頁面](event-reference-page.md)。</span><span class="sxs-lookup"><span data-stu-id="3046d-112">For more information about the creation of HTML-based configuration information, see [Event Reference Page](event-reference-page.md).</span></span>

<span data-ttu-id="3046d-113">在網路監視器設定期間，會在專家子目錄中安裝下列專家 Dll：</span><span class="sxs-lookup"><span data-stu-id="3046d-113">During Network Monitor setup, the following expert DLLs are installed in the Experts sub-directory:</span></span>

-   <span data-ttu-id="3046d-114">Coalesce.dll</span><span class="sxs-lookup"><span data-stu-id="3046d-114">Coalesce.dll</span></span>
-   <span data-ttu-id="3046d-115">Propdist.dll</span><span class="sxs-lookup"><span data-stu-id="3046d-115">Propdist.dll</span></span>
-   <span data-ttu-id="3046d-116">Protdist.dll</span><span class="sxs-lookup"><span data-stu-id="3046d-116">Protdist.dll</span></span>
-   <span data-ttu-id="3046d-117">Resptime.dll</span><span class="sxs-lookup"><span data-stu-id="3046d-117">Resptime.dll</span></span>
-   <span data-ttu-id="3046d-118">Tcpipe.dll</span><span class="sxs-lookup"><span data-stu-id="3046d-118">Tcpipe.dll</span></span>
-   <span data-ttu-id="3046d-119">Topuser.dll</span><span class="sxs-lookup"><span data-stu-id="3046d-119">Topuser.dll</span></span>

<span data-ttu-id="3046d-120">當您開始網路監視器時， [**DllMain**](dllmain-expert.md) 函式會建立專家子目錄中的所有專家。</span><span class="sxs-lookup"><span data-stu-id="3046d-120">When you start Network Monitor, the [**DllMain**](dllmain-expert.md) function builds all experts in the experts subdirectory.</span></span> <span data-ttu-id="3046d-121">當使用者在網路監視器 UI 的 [**工具**] 功能表上選取 **專家** 時，網路監視器載入專家 dll。</span><span class="sxs-lookup"><span data-stu-id="3046d-121">When the user selects **Experts** on the **Tools** menu of the Network Monitor UI, Network Monitor loads the expert DLLs.</span></span> <span data-ttu-id="3046d-122">專家是透過 [註冊專家](register-expert.md) 進入點來呼叫，以提供專家的基本詳細資料。</span><span class="sxs-lookup"><span data-stu-id="3046d-122">The expert is called through the [Register Expert](register-expert.md) entry point to provide basic details about the expert.</span></span>

![網路監視器專家對話方塊](images/expick.png)

<span data-ttu-id="3046d-124">網路監視器會呼叫下列函數來管理專家：</span><span class="sxs-lookup"><span data-stu-id="3046d-124">Network Monitor calls the following functions to manage the expert:</span></span>

-   [<span data-ttu-id="3046d-125">**DllMain**</span><span class="sxs-lookup"><span data-stu-id="3046d-125">**DllMain**</span></span>](dllmain-expert.md)
-   [<span data-ttu-id="3046d-126">**註冊專家**</span><span class="sxs-lookup"><span data-stu-id="3046d-126">**Register Expert**</span></span>](register-expert.md)
-   [<span data-ttu-id="3046d-127">**執行**</span><span class="sxs-lookup"><span data-stu-id="3046d-127">**Run**</span></span>](run.md)
-   [<span data-ttu-id="3046d-128">**設定**</span><span class="sxs-lookup"><span data-stu-id="3046d-128">**Configure**</span></span>](configure.md)

<span data-ttu-id="3046d-129">專家必須執行上述各項功能。</span><span class="sxs-lookup"><span data-stu-id="3046d-129">The expert must implement each of the preceding functions.</span></span>

 

 



