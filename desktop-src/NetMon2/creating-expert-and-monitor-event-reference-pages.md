---
description: 本節說明如何規劃、開發及測試事件參考頁面 (ERPs) 以及如何在專家或監視器中部署它們。 如需有關 ERPs 以及如何搭配網路監視器使用它們的詳細資訊，請參閱事件參考頁面。
ms.assetid: 78d6e8cf-785e-4d5f-a78d-9ef9da9bc3e0
title: 建立專家和監視事件參考頁面
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33c84610c7a1088e994fc852c64a7893f73f7909
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106985444"
---
# <a name="creating-expert-and-monitor-event-reference-pages"></a><span data-ttu-id="f9a14-104">建立專家和監視事件參考頁面</span><span class="sxs-lookup"><span data-stu-id="f9a14-104">Creating Expert and Monitor Event Reference Pages</span></span>

<span data-ttu-id="f9a14-105">本節說明如何規劃、開發及測試事件參考頁面 (ERPs) 以及如何在專家或監視器中部署它們。</span><span class="sxs-lookup"><span data-stu-id="f9a14-105">This section describes how to plan, develop, and test event reference pages (ERPs) and how to deploy them in an expert or monitor.</span></span> <span data-ttu-id="f9a14-106">如需有關 ERPs 以及如何搭配網路監視器使用它們的詳細資訊，請參閱 [事件參考頁面](event-reference-page.md)。</span><span class="sxs-lookup"><span data-stu-id="f9a14-106">For information about ERPs and how to use them with Network Monitor, see [Event Reference Page](event-reference-page.md).</span></span>

<span data-ttu-id="f9a14-107">若要開發新的 ERP，第一個步驟是判斷需要個別 ERPs 給自訂 [專家](experts.md) 或 [監視器](monitors.md)的事件。</span><span class="sxs-lookup"><span data-stu-id="f9a14-107">To develop a new ERP, the first step is determining the events that require individual ERPs for your custom [expert](experts.md) or [monitor](monitors.md).</span></span> <span data-ttu-id="f9a14-108">您必須針對想要顯示在網路監視器事件檢視器中的每個事件建立個別的 ERPs。</span><span class="sxs-lookup"><span data-stu-id="f9a14-108">You must create separate ERPs for each event you wish to display in the Network Monitor Event Viewer.</span></span> <span data-ttu-id="f9a14-109">例如，假設：</span><span class="sxs-lookup"><span data-stu-id="f9a14-109">For example, suppose that:</span></span>

-   <span data-ttu-id="f9a14-110">您會開發一個名為遊戲監視器和股票監看員的監視器。</span><span class="sxs-lookup"><span data-stu-id="f9a14-110">You develop a monitor named Game Monitor and Stock Watcher.</span></span>
-   <span data-ttu-id="f9a14-111">此監視器位於稱為 Gamemon.dll 的檔案中。</span><span class="sxs-lookup"><span data-stu-id="f9a14-111">The monitor is located in a file called Gamemon.dll.</span></span>
-   <span data-ttu-id="f9a14-112">此監視器會產生兩個事件：執行遊戲的遊戲和我的網際網路股票 Soars。</span><span class="sxs-lookup"><span data-stu-id="f9a14-112">The monitor generates two events, Game Running and My Internet Stock Soars.</span></span>
-   <span data-ttu-id="f9a14-113">您打算開發兩個 ERPs、Gamemon1.htm 和 Gamemon2.htm。</span><span class="sxs-lookup"><span data-stu-id="f9a14-113">You plan to develop two ERPs, Gamemon1.htm and Gamemon2.htm.</span></span>

> [!Note]  
> <span data-ttu-id="f9a14-114">不需要 ERPs 的一對一對應來監視或專家的活動。</span><span class="sxs-lookup"><span data-stu-id="f9a14-114">It's not necessary to have a one-to-one correspondence of ERPs to monitor or expert events.</span></span>

 

<span data-ttu-id="f9a14-115">建立唯一 ERPs 清單之後，請遵循下列步驟來建立每個 ERP。</span><span class="sxs-lookup"><span data-stu-id="f9a14-115">After you have established a list of unique ERPs, follow these steps to create each ERP.</span></span>

-   <span data-ttu-id="f9a14-116">[撰寫 HTML 來源文件](writing-an-event-reference-page.md)。</span><span class="sxs-lookup"><span data-stu-id="f9a14-116">[Write the HTML source document](writing-an-event-reference-page.md).</span></span>
-   <span data-ttu-id="f9a14-117">將 HTML 原始程式檔[儲存並命名](naming-an-event-reference-page.md)為 .htm 檔。</span><span class="sxs-lookup"><span data-stu-id="f9a14-117">[Save and name](naming-an-event-reference-page.md) the HTML source file as an .htm file.</span></span>
-   <span data-ttu-id="f9a14-118">使用已完成的專家或監視器來[測試 ERP](testing-an-event-reference-page.md) 。</span><span class="sxs-lookup"><span data-stu-id="f9a14-118">[Test the ERP](testing-an-event-reference-page.md) with the completed expert or monitor.</span></span>

 

 



