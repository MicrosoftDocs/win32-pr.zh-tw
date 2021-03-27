---
description: 根據預設，當 Windows 以安全模式執行時，不會顯示 Windows Vista 主控台專案。
title: 以安全模式存取主控台
ms.topic: article
ms.date: 05/31/2018
ms.assetid: f37bcb0f-9417-4cc4-a57d-4f67a9ccda19
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 0f7a401bbc22a7f8de3618f844bfe463fa3baa50
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972080"
---
# <a name="accessing-the-control-panel-in-safe-mode"></a><span data-ttu-id="88627-103">以安全模式存取主控台</span><span class="sxs-lookup"><span data-stu-id="88627-103">Accessing the Control Panel in Safe Mode</span></span>

<span data-ttu-id="88627-104">根據預設，當 Windows 以安全模式執行時，不會顯示 Windows Vista 主控台專案。</span><span class="sxs-lookup"><span data-stu-id="88627-104">By default, as of Windows Vista Control Panel items are not shown when Windows is run in safe mode.</span></span> <span data-ttu-id="88627-105">若要允許以安全模式來查看新的主控台專案，可以設定適用于專案類型的登錄值。</span><span class="sxs-lookup"><span data-stu-id="88627-105">To allow a new Control Panel item to be viewed in safe mode, registry values appropriate to the item type can be set.</span></span> <span data-ttu-id="88627-106">這些值會以下列方式解讀：</span><span class="sxs-lookup"><span data-stu-id="88627-106">The values are interpreted as follows:</span></span>



| <span data-ttu-id="88627-107">值</span><span class="sxs-lookup"><span data-stu-id="88627-107">Value</span></span> | <span data-ttu-id="88627-108">意義</span><span class="sxs-lookup"><span data-stu-id="88627-108">Meaning</span></span>                                                            |
|-------|--------------------------------------------------------------------|
| <span data-ttu-id="88627-109">1</span><span class="sxs-lookup"><span data-stu-id="88627-109">1</span></span>     | <span data-ttu-id="88627-110">專案只應以最小的安全模式顯示。</span><span class="sxs-lookup"><span data-stu-id="88627-110">The item should appear in minimal safe mode only.</span></span>                  |
| <span data-ttu-id="88627-111">2</span><span class="sxs-lookup"><span data-stu-id="88627-111">2</span></span>     | <span data-ttu-id="88627-112">只有在已啟用網路功能的情況下，專案才會顯示在安全模式中。</span><span class="sxs-lookup"><span data-stu-id="88627-112">The item should appear in safe mode only if networking is enabled.</span></span> |
| <span data-ttu-id="88627-113">3</span><span class="sxs-lookup"><span data-stu-id="88627-113">3</span></span>     | <span data-ttu-id="88627-114">專案應一律以任何形式的安全模式顯示。</span><span class="sxs-lookup"><span data-stu-id="88627-114">The item should always appear in any form of safe mode.</span></span>            |



 

<span data-ttu-id="88627-115">這個範例會顯示實作為 cpl 或 .dll 檔案的專案所需的專案。</span><span class="sxs-lookup"><span data-stu-id="88627-115">This example shows the entries required for an item implemented as a .cpl or .dll file.</span></span> <span data-ttu-id="88627-116">它會指定專案應以具有網路功能的安全模式顯示。</span><span class="sxs-lookup"><span data-stu-id="88627-116">It specifies that the item should appear in safe mode with networking.</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Control Panel
                  Extended Properties
                     System.ControlPanel.EnableInSafeMode
                        %ProgramFiles%\MyCorp\MyApp\MyCpl.cpl = [REG_DWORD] 2
```

<span data-ttu-id="88627-117">這個範例會顯示實作為 .exe 檔的專案所需的專案。</span><span class="sxs-lookup"><span data-stu-id="88627-117">This example shows the entries required for an item implemented as a .exe file.</span></span> <span data-ttu-id="88627-118">它指定專案應以任何形式的安全模式顯示。</span><span class="sxs-lookup"><span data-stu-id="88627-118">It specifies that the item should appear in any form of safe mode.</span></span>

```
HKEY_CLASSES_ROOT
   CLSID
      {0052D9FC-6764-4D29-A66F-2F3BD9E2BB40}
         System.ControlPanel.EnableInSafeMode = [REG_DWORD] 3
```

## <a name="related-topics"></a><span data-ttu-id="88627-119">相關主題</span><span class="sxs-lookup"><span data-stu-id="88627-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="88627-120">主控台專案</span><span class="sxs-lookup"><span data-stu-id="88627-120">Control Panel Items</span></span>](control-panel-applications.md)
</dt> <dt>

[<span data-ttu-id="88627-121">使用者體驗指南</span><span class="sxs-lookup"><span data-stu-id="88627-121">User Experience Guidelines</span></span>](user-experience-guidelines.md)
</dt> <dt>

[<span data-ttu-id="88627-122">註冊主控台專案</span><span class="sxs-lookup"><span data-stu-id="88627-122">Registering Control Panel Items</span></span>](registering-control-panel-items.md)
</dt> <dt>

[<span data-ttu-id="88627-123">使用 CPLApplet</span><span class="sxs-lookup"><span data-stu-id="88627-123">Using CPLApplet</span></span>](using-cplapplet.md)
</dt> <dt>

[<span data-ttu-id="88627-124">主控台訊息處理</span><span class="sxs-lookup"><span data-stu-id="88627-124">Control Panel Message Processing</span></span>](message-processing.md)
</dt> <dt>

[<span data-ttu-id="88627-125">執行主控台專案</span><span class="sxs-lookup"><span data-stu-id="88627-125">Executing Control Panel Items</span></span>](executing-control-panel-items.md)
</dt> <dt>

[<span data-ttu-id="88627-126">擴充系統主控台專案</span><span class="sxs-lookup"><span data-stu-id="88627-126">Extending System Control Panel Items</span></span>](extending-system-control-panel-items.md)
</dt> <dt>

[<span data-ttu-id="88627-127">指派主控台分類</span><span class="sxs-lookup"><span data-stu-id="88627-127">Assigning Control Panel Categories</span></span>](assigning-control-panel-categories.md)
</dt> <dt>

[<span data-ttu-id="88627-128">建立主控台專案的可搜尋工作連結</span><span class="sxs-lookup"><span data-stu-id="88627-128">Creating Searchable Task Links for a Control Panel Item</span></span>](creating-searchable-task-links.md)
</dt> </dl>

 

 



