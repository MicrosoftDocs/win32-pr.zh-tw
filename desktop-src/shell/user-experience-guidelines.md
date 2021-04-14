---
description: 任何主控台專案的主要責任是顯示一個視窗，讓使用者能夠查看和操作設定。
title: 使用者體驗指南
ms.topic: article
ms.date: 09/24/2020
ms.assetid: f03a154b-9781-4718-8244-3d57fee0755e
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: e25f8885c2444a51d5d5d8cc917121c7f3b26a09
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104991774"
---
# <a name="user-experience-guidelines"></a><span data-ttu-id="78deb-103">使用者體驗指南</span><span class="sxs-lookup"><span data-stu-id="78deb-103">User Experience Guidelines</span></span>

<span data-ttu-id="78deb-104">任何主控台專案的主要責任是顯示一個視窗，讓使用者能夠查看和操作設定。</span><span class="sxs-lookup"><span data-stu-id="78deb-104">The primary responsibility of any Control Panel item is to display a window that allows the user to view and manipulate settings.</span></span> <span data-ttu-id="78deb-105">請參閱 [控制項面板使用者體驗 (UX) 指導方針](../uxguide/winenv-ctrl-panels.md) ，以瞭解主控台專案的行為與設計。</span><span class="sxs-lookup"><span data-stu-id="78deb-105">See the [Control Panels user experience (UX) guidelines](../uxguide/winenv-ctrl-panels.md) for the behavior and design of Control Panel items.</span></span> <span data-ttu-id="78deb-106">本主題所討論的指導方針會顯示組織主控台專案的工作流程方法。</span><span class="sxs-lookup"><span data-stu-id="78deb-106">The guidelines discussed in that topic show a task flow method of organizing a Control Panel item.</span></span> <span data-ttu-id="78deb-107">這會將最重要的設定放在首頁上。</span><span class="sxs-lookup"><span data-stu-id="78deb-107">This places the most important settings on a home page.</span></span> <span data-ttu-id="78deb-108">較不常使用的設定會放在輪輻頁面上，或從側邊窗格中的連結存取。</span><span class="sxs-lookup"><span data-stu-id="78deb-108">Less frequently used settings are placed on spoke pages or accessed from links in a side pane.</span></span>

<span data-ttu-id="78deb-109">主控台包含許多遵循這些指導方針的專案，例如輕鬆存取中心和網路和共用中心。</span><span class="sxs-lookup"><span data-stu-id="78deb-109">The Control Panel includes many items that follow these guidelines, such as Ease of Access Center and Network and Sharing Center.</span></span> <span data-ttu-id="78deb-110">其他主控台專案使用索引標籤式對話方塊屬性工作表格式，如同舊版 Windows 一樣。</span><span class="sxs-lookup"><span data-stu-id="78deb-110">Other Control Panel items use the tabbed dialog property sheet format as in earlier versions of Windows.</span></span> <span data-ttu-id="78deb-111">範例包括滑鼠專案和網際網路選項。</span><span class="sxs-lookup"><span data-stu-id="78deb-111">Examples include the Mouse item and Internet Options.</span></span> <span data-ttu-id="78deb-112">應停止使用屬性工作表格式。</span><span class="sxs-lookup"><span data-stu-id="78deb-112">Use of the property sheet format should be discontinued.</span></span> <span data-ttu-id="78deb-113">如果您建立新的主控台專案，則應遵循工作流程指導方針。</span><span class="sxs-lookup"><span data-stu-id="78deb-113">If you create new Control Panel items, you should follow the task flow guidelines.</span></span>

<span data-ttu-id="78deb-114">在過去，主控台專案封裝為 cpl 檔。</span><span class="sxs-lookup"><span data-stu-id="78deb-114">In the past, Control Panel items were packaged as .cpl files.</span></span> <span data-ttu-id="78deb-115">不再需要。</span><span class="sxs-lookup"><span data-stu-id="78deb-115">That is no longer necessary.</span></span> <span data-ttu-id="78deb-116">新的主控台專案應實作為獨立 .exe 檔，或做為應用程式主要可執行檔的命令列旗標選項。</span><span class="sxs-lookup"><span data-stu-id="78deb-116">New Control Panel items should be implemented as a standalone .exe file or as a command-line flag option for the application's main executable file.</span></span>

> [!Note]  
> <span data-ttu-id="78deb-117">在64位系統上，當選取 **View 32-bit 主控台 items 資料夾** 選項時，主控台會顯示32位主控台專案。</span><span class="sxs-lookup"><span data-stu-id="78deb-117">On 64-bit systems, 32-bit Control Panel items are displayed in the Control Panel when the **View 32-bit Control Panel Items folder** option is selected.</span></span> <span data-ttu-id="78deb-118">32位專案必須位於要顯示的% SystemRoot% \\ SysWOW64 資料夾中。</span><span class="sxs-lookup"><span data-stu-id="78deb-118">The 32-bit items must be located in the %SystemRoot%\\SysWOW64 folder to be displayed.</span></span> <span data-ttu-id="78deb-119">它們不需要任何進一步的註冊。</span><span class="sxs-lookup"><span data-stu-id="78deb-119">They do not require any further registration.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="78deb-120">相關主題</span><span class="sxs-lookup"><span data-stu-id="78deb-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="78deb-121">主控台專案</span><span class="sxs-lookup"><span data-stu-id="78deb-121">Control Panel Items</span></span>](control-panel-applications.md)
</dt> <dt>

[<span data-ttu-id="78deb-122">註冊主控台專案</span><span class="sxs-lookup"><span data-stu-id="78deb-122">Registering Control Panel Items</span></span>](registering-control-panel-items.md)
</dt> <dt>

[<span data-ttu-id="78deb-123">使用 CPLApplet</span><span class="sxs-lookup"><span data-stu-id="78deb-123">Using CPLApplet</span></span>](using-cplapplet.md)
</dt> <dt>

[<span data-ttu-id="78deb-124">主控台訊息處理</span><span class="sxs-lookup"><span data-stu-id="78deb-124">Control Panel Message Processing</span></span>](message-processing.md)
</dt> <dt>

[<span data-ttu-id="78deb-125">執行主控台專案</span><span class="sxs-lookup"><span data-stu-id="78deb-125">Executing Control Panel Items</span></span>](executing-control-panel-items.md)
</dt> <dt>

[<span data-ttu-id="78deb-126">擴充系統主控台專案</span><span class="sxs-lookup"><span data-stu-id="78deb-126">Extending System Control Panel Items</span></span>](extending-system-control-panel-items.md)
</dt> <dt>

[<span data-ttu-id="78deb-127">指派主控台分類</span><span class="sxs-lookup"><span data-stu-id="78deb-127">Assigning Control Panel Categories</span></span>](assigning-control-panel-categories.md)
</dt> <dt>

[<span data-ttu-id="78deb-128">建立主控台專案的可搜尋工作連結</span><span class="sxs-lookup"><span data-stu-id="78deb-128">Creating Searchable Task Links for a Control Panel Item</span></span>](creating-searchable-task-links.md)
</dt> <dt>

[<span data-ttu-id="78deb-129">以安全模式存取主控台</span><span class="sxs-lookup"><span data-stu-id="78deb-129">Accessing the Control Panel in Safe Mode</span></span>](accessing-the-cp-in-safe-mode-under-vista.md)
</dt> </dl>

 

 



