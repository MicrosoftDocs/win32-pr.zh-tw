---
title: 開始下載
description: 開始下載
ms.assetid: 0a830b11-f7e1-41da-a867-86f9ac361c0b
keywords:
- Windows Media Player 線上商店，下載管理員
- 線上商店、下載管理員
- 輸入2個線上商店、下載管理員
- Windows Media Player 線上商店，開始下載
- 線上商店，開始下載
- 輸入2個線上商店，開始下載
- Windows Media Player，下載管理員
- Windows Media Player 下載管理員
- 下載管理員
- 開始下載
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cec723bd504cc511c3ca43db90f3c613a8acefd1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104372573"
---
# <a name="starting-the-downloads"></a><span data-ttu-id="027bc-113">開始下載</span><span class="sxs-lookup"><span data-stu-id="027bc-113">Starting the Downloads</span></span>

<span data-ttu-id="027bc-114">當使用者按一下 [ **下載**] 時，就會開始下載。</span><span class="sxs-lookup"><span data-stu-id="027bc-114">The downloading starts when the user clicks **Download**.</span></span> <span data-ttu-id="027bc-115">此按鈕在程式碼中名為 btnDownload，而 **onClick** 事件的事件處理常式函式會命名為 "OnDownload"。</span><span class="sxs-lookup"><span data-stu-id="027bc-115">This button is named btnDownload in the code and the event handler function for the **onClick** event is named "OnDownload".</span></span>

<span data-ttu-id="027bc-116">"OnDownload" 會先建立新的空白 **DownloadCollection** 物件，並將它指派給本機變數。</span><span class="sxs-lookup"><span data-stu-id="027bc-116">"OnDownload" first creates a new empty **DownloadCollection** object and assigns it to a local variable.</span></span>


```C++
oDLC = g_oManager.createDownloadCollection();

```



<span data-ttu-id="027bc-117">接下來，此函式會啟動每五個專案的下載，並將傳回的 **DownloadItem** 物件儲存在陣列中。</span><span class="sxs-lookup"><span data-stu-id="027bc-117">Next, the function starts each of the five items downloading and stores the returned **DownloadItem** object in an array.</span></span>


```C++
g_DLI[0] = oDLC.startDownload(g_sFiles[0], g_sDLType);
g_DLI[1] = oDLC.startDownload(g_sFiles[1], g_sDLType);
g_DLI[2] = oDLC.startDownload(g_sFiles[2], g_sDLType);
g_DLI[3] = oDLC.startDownload(g_sFiles[3], g_sDLType);
g_DLI[4] = oDLC.startDownload(g_sFiles[4], g_sDLType);

```



<span data-ttu-id="027bc-118">然後，程式碼會使用下載集合及其下載專案的相關資訊來更新使用者介面元素。</span><span class="sxs-lookup"><span data-stu-id="027bc-118">The code then updates the user interface elements with the information about the download collection and its download items.</span></span>

## <a name="related-topics"></a><span data-ttu-id="027bc-119">相關主題</span><span class="sxs-lookup"><span data-stu-id="027bc-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="027bc-120">**使用下載管理員**</span><span class="sxs-lookup"><span data-stu-id="027bc-120">**Using the Download Manager**</span></span>](using-the-download-manager.md)
</dt> </dl>

 

 




