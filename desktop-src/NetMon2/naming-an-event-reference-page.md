---
description: 在 (ERP) 原始檔 HTML 檔案中撰寫事件參考頁面之後，您必須先將它命名，才能網路監視器可以在事件檢視器中顯示。
ms.assetid: 0c668a8b-94a5-4996-8214-4629a24a8337
title: 命名事件參考頁面
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f9c82b153ce2c7086af3883bcf3c4b34a0e68a6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106991375"
---
# <a name="naming-an-event-reference-page"></a><span data-ttu-id="779ac-103">命名事件參考頁面</span><span class="sxs-lookup"><span data-stu-id="779ac-103">Naming an Event Reference Page</span></span>

<span data-ttu-id="779ac-104">在 (ERP) 原始檔 HTML 檔案中撰寫事件參考頁面之後，您必須先將它命名，才能網路監視器可以在事件檢視器中顯示。</span><span class="sxs-lookup"><span data-stu-id="779ac-104">After you author an event reference page (ERP) source HTML document, you must name it before Network Monitor can display it in the Event Viewer.</span></span>

<span data-ttu-id="779ac-105">使用下列格式的名稱監視和專家 ERP 檔案：</span><span class="sxs-lookup"><span data-stu-id="779ac-105">Name monitor and expert ERP files with this format:</span></span>

``` syntax
<ExpertName><EventIdent>.htm (or <MonitorName><EventIdent>.htm)
```

<dl> <dt>

<span data-ttu-id="779ac-106"><span id="ExpertName"></span><span id="expertname"></span><span id="EXPERTNAME"></span>**ExpertName**</span><span class="sxs-lookup"><span data-stu-id="779ac-106"><span id="ExpertName"></span><span id="expertname"></span><span id="EXPERTNAME"></span>**ExpertName**</span></span>
</dt> <dd>

<span data-ttu-id="779ac-107">DLL 檔案名，但不含副檔名。</span><span class="sxs-lookup"><span data-stu-id="779ac-107">DLL file name, excluding the file name extension.</span></span>

</dd> <dt>

<span data-ttu-id="779ac-108"><span id="EventIdent"></span><span id="eventident"></span><span id="EVENTIDENT"></span>**EventIdent**</span><span class="sxs-lookup"><span data-stu-id="779ac-108"><span id="EventIdent"></span><span id="eventident"></span><span id="EVENTIDENT"></span>**EventIdent**</span></span>
</dt> <dd>

<span data-ttu-id="779ac-109">專家 ERP 的事件識別碼。</span><span class="sxs-lookup"><span data-stu-id="779ac-109">Event identifier of the expert ERP.</span></span>

<span data-ttu-id="779ac-110">事件識別碼也可以在 **NMEVENTDATA** 結構的 **EventIdent** 成員中找到。</span><span class="sxs-lookup"><span data-stu-id="779ac-110">The event identifier is also found in the **EventIdent** member of the **NMEVENTDATA** structure.</span></span>

</dd> </dl>

<span data-ttu-id="779ac-111">如需有關建立 ERP 的詳細資訊，請參閱下列主題：</span><span class="sxs-lookup"><span data-stu-id="779ac-111">For more information about creating an ERP, see the following topics:</span></span>

-   [<span data-ttu-id="779ac-112">建立專家和監視事件參考頁面</span><span class="sxs-lookup"><span data-stu-id="779ac-112">Creating Expert and Monitor Event Reference Pages</span></span>](creating-expert-and-monitor-event-reference-pages.md)
-   [<span data-ttu-id="779ac-113">撰寫事件參考頁面</span><span class="sxs-lookup"><span data-stu-id="779ac-113">Writing an Event Reference Page</span></span>](writing-an-event-reference-page.md)
-   [<span data-ttu-id="779ac-114">測試事件參考頁面</span><span class="sxs-lookup"><span data-stu-id="779ac-114">Testing an Event Reference Page</span></span>](testing-an-event-reference-page.md)

 

 



