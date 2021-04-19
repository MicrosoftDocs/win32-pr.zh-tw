---
description: " (ERP) 建立事件參考頁面的最後一個步驟是進行測試。"
ms.assetid: 12690317-1cd2-496c-8a0d-ba6caca58b86
title: 測試事件參考頁面
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6afaaec279403922abde578b9e73931e607680f8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970209"
---
# <a name="testing-an-event-reference-page"></a><span data-ttu-id="5b43d-103">測試事件參考頁面</span><span class="sxs-lookup"><span data-stu-id="5b43d-103">Testing an Event Reference Page</span></span>

<span data-ttu-id="5b43d-104"> (ERP) 建立事件參考頁面的最後一個步驟是進行測試。</span><span class="sxs-lookup"><span data-stu-id="5b43d-104">The final step of creating an event reference page (ERP) is to test it.</span></span> <span data-ttu-id="5b43d-105">您可以在 HTML 瀏覽器（例如 Microsoft Internet Explorer）中查看檔案，以測試 ERP。</span><span class="sxs-lookup"><span data-stu-id="5b43d-105">You can test an ERP by viewing the file in an HTML browser such as Microsoft Internet Explorer.</span></span> <span data-ttu-id="5b43d-106">或者，您可以安裝 ERP 和其專家 DLL 來測試事件調用，並將其顯示在網路監視器事件檢視器中。</span><span class="sxs-lookup"><span data-stu-id="5b43d-106">Or, you can install the ERP and its expert DLL to test it for event invocation and display it in the Network Monitor Event Viewer.</span></span>

## <a name="viewing-erps-that-have-no-dll"></a><span data-ttu-id="5b43d-107">查看沒有 DLL 的 ERPs</span><span class="sxs-lookup"><span data-stu-id="5b43d-107">Viewing ERPs that Have No DLL</span></span>

<span data-ttu-id="5b43d-108">若要在沒有已安裝專家 DLL 的情況下查看已完成的 ERP，請使用支援內嵌來源的 HTML 檢視器來開啟檔案。</span><span class="sxs-lookup"><span data-stu-id="5b43d-108">To view the completed ERP without an installed expert DLL, open the file with an HTML viewer that supports your embedded sources.</span></span> <span data-ttu-id="5b43d-109">下圖顯示在使用 Microsoft Internet Explorer 4.01 版顯示的情況下 [撰寫 erp](writing-an-event-reference-page.md) 時所述的 erp 檔案範例。</span><span class="sxs-lookup"><span data-stu-id="5b43d-109">The following illustration shows the sample ERP file described in [Writing an ERP](writing-an-event-reference-page.md) as it is displayed using Microsoft Internet Explorer Version 4.01.</span></span>

![範例 erp 檔案](images/ie-erp.png)

<span data-ttu-id="5b43d-111">測試具有 DLL 的 ERPs</span><span class="sxs-lookup"><span data-stu-id="5b43d-111">Testing ERPs that Have a DLL</span></span>

<span data-ttu-id="5b43d-112">建立 ERP 檔案和 [**專家**](experts.md) DLL 之後，您就可以使用網路監視器來測試 ERPs 的完整功能。</span><span class="sxs-lookup"><span data-stu-id="5b43d-112">After the ERP files and the [**expert**](experts.md) DLL is created, you can test the complete functionality of your ERPs with Network Monitor.</span></span> <span data-ttu-id="5b43d-113">假設 DLL 已進行調試，而且可以產生有效的事件。</span><span class="sxs-lookup"><span data-stu-id="5b43d-113">It is assumed that the DLL is debugged and can generate valid events.</span></span>

<span data-ttu-id="5b43d-114">**若要測試具有 DLL 的 ERPs**</span><span class="sxs-lookup"><span data-stu-id="5b43d-114">**To test ERPs that have a DLL**</span></span>

1.  <span data-ttu-id="5b43d-115">確認正確的專家 DLL 已安裝在適當的目錄中。</span><span class="sxs-lookup"><span data-stu-id="5b43d-115">Verify that the correct expert DLL is installed in the appropriate directory.</span></span> <span data-ttu-id="5b43d-116">如需詳細資訊，請參閱 [安裝專家至網路監視器 2.1](installing-an-expert-to-network-monitor-2-1.md)。</span><span class="sxs-lookup"><span data-stu-id="5b43d-116">For more information, see [Installing an Expert to Network Monitor 2.1](installing-an-expert-to-network-monitor-2-1.md).</span></span>
2.  <span data-ttu-id="5b43d-117">驗證 ERP 檔案的 [正確名稱](naming-an-event-reference-page.md) 。</span><span class="sxs-lookup"><span data-stu-id="5b43d-117">Verify the [correct name](naming-an-event-reference-page.md) of the ERP file.</span></span>
3.  <span data-ttu-id="5b43d-118">確認網路監視器目錄中的 ERPs [正確位置](installing-existing-erps-to-network-monitor-2-1.md) 。</span><span class="sxs-lookup"><span data-stu-id="5b43d-118">Verify the [correct location](installing-existing-erps-to-network-monitor-2-1.md) of the ERPs in the Network Monitor directory.</span></span>
4.  <span data-ttu-id="5b43d-119">測試網路監視器 UI 中的專家 ERPs。</span><span class="sxs-lookup"><span data-stu-id="5b43d-119">Test expert ERPs in the Network Monitor UI.</span></span>
5.  <span data-ttu-id="5b43d-120">產生測試事件。</span><span class="sxs-lookup"><span data-stu-id="5b43d-120">Generate a test event.</span></span>
6.  <span data-ttu-id="5b43d-121">確認 ERP 出現在網路監視器事件檢視器中。</span><span class="sxs-lookup"><span data-stu-id="5b43d-121">Verify that the ERP appears in the Network Monitor Event Viewer.</span></span>

<span data-ttu-id="5b43d-122">如需有關建立 ERP 的詳細資訊，請參閱：</span><span class="sxs-lookup"><span data-stu-id="5b43d-122">For more information about creating an ERP, see:</span></span>

-   [<span data-ttu-id="5b43d-123">建立專家和監視事件參考頁面</span><span class="sxs-lookup"><span data-stu-id="5b43d-123">Creating Expert and Monitor Event Reference Pages</span></span>](creating-expert-and-monitor-event-reference-pages.md)
-   [<span data-ttu-id="5b43d-124">撰寫事件參考頁面</span><span class="sxs-lookup"><span data-stu-id="5b43d-124">Writing an Event Reference Page</span></span>](writing-an-event-reference-page.md)
-   [<span data-ttu-id="5b43d-125">命名事件參考頁面</span><span class="sxs-lookup"><span data-stu-id="5b43d-125">Naming an Event Reference Page</span></span>](naming-an-event-reference-page.md)

 

 



