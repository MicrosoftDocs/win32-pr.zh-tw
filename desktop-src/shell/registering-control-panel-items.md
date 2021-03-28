---
description: 主控台專案必須註冊，才能出現在 [主控台] 視窗中。
title: 註冊主控台專案
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 6f21f223-a293-47b5-95e9-06b7a4ff1652
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 05c2a652314babc212e17b48198e9441f4d3465d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104115728"
---
# <a name="registering-control-panel-items"></a><span data-ttu-id="4e2e8-103">註冊主控台專案</span><span class="sxs-lookup"><span data-stu-id="4e2e8-103">Registering Control Panel Items</span></span>

<span data-ttu-id="4e2e8-104">主控台專案必須註冊，才能出現在 [主控台] 視窗中。</span><span class="sxs-lookup"><span data-stu-id="4e2e8-104">Control Panel items must be registered in order to appear in the Control Panel window.</span></span> <span data-ttu-id="4e2e8-105">如果主控台專案實作為 .exe 檔案的一部分，則會將它註冊為 command 物件。</span><span class="sxs-lookup"><span data-stu-id="4e2e8-105">If the Control Panel item is implemented as part of a .exe file then it is registered as a command object.</span></span> <span data-ttu-id="4e2e8-106">如果專案實作為匯出 [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) 函式的 .dll 檔案，則註冊會有所不同。</span><span class="sxs-lookup"><span data-stu-id="4e2e8-106">Registration differs if the item is implemented as a .dll file that exports the [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) function.</span></span>

<span data-ttu-id="4e2e8-107">這些主題會討論特定的需求：</span><span class="sxs-lookup"><span data-stu-id="4e2e8-107">Specific requirements are discussed in these topics:</span></span>

-   [<span data-ttu-id="4e2e8-108">如何註冊可執行檔主控台專案</span><span class="sxs-lookup"><span data-stu-id="4e2e8-108">How To Register Executable Control Panel Items</span></span>](how-to-register-an-executable-control-panel-item-registration-.md)
-   [<span data-ttu-id="4e2e8-109">如何註冊 DLL 主控台專案</span><span class="sxs-lookup"><span data-stu-id="4e2e8-109">How To Register DLL Control Panel Items</span></span>](how-to-register-dll-control-panel-item-registration-.md)

## <a name="related-topics"></a><span data-ttu-id="4e2e8-110">相關主題</span><span class="sxs-lookup"><span data-stu-id="4e2e8-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4e2e8-111">主控台專案</span><span class="sxs-lookup"><span data-stu-id="4e2e8-111">Control Panel Items</span></span>](control-panel-applications.md)
</dt> <dt>

[<span data-ttu-id="4e2e8-112">使用者體驗指南</span><span class="sxs-lookup"><span data-stu-id="4e2e8-112">User Experience Guidelines</span></span>](user-experience-guidelines.md)
</dt> <dt>

[<span data-ttu-id="4e2e8-113">使用 CPLApplet</span><span class="sxs-lookup"><span data-stu-id="4e2e8-113">Using CPLApplet</span></span>](using-cplapplet.md)
</dt> <dt>

[<span data-ttu-id="4e2e8-114">主控台訊息處理</span><span class="sxs-lookup"><span data-stu-id="4e2e8-114">Control Panel Message Processing</span></span>](message-processing.md)
</dt> <dt>

[<span data-ttu-id="4e2e8-115">執行主控台專案</span><span class="sxs-lookup"><span data-stu-id="4e2e8-115">Executing Control Panel Items</span></span>](executing-control-panel-items.md)
</dt> <dt>

[<span data-ttu-id="4e2e8-116">擴充系統主控台專案</span><span class="sxs-lookup"><span data-stu-id="4e2e8-116">Extending System Control Panel Items</span></span>](extending-system-control-panel-items.md)
</dt> <dt>

[<span data-ttu-id="4e2e8-117">指派主控台分類</span><span class="sxs-lookup"><span data-stu-id="4e2e8-117">Assigning Control Panel Categories</span></span>](assigning-control-panel-categories.md)
</dt> <dt>

[<span data-ttu-id="4e2e8-118">建立主控台專案的可搜尋工作連結</span><span class="sxs-lookup"><span data-stu-id="4e2e8-118">Creating Searchable Task Links for a Control Panel Item</span></span>](creating-searchable-task-links.md)
</dt> <dt>

[<span data-ttu-id="4e2e8-119">在 Windows Vista 下存取安全模式下的主控台</span><span class="sxs-lookup"><span data-stu-id="4e2e8-119">Accessing the Control Panel in Safe Mode under Windows Vista</span></span>](accessing-the-cp-in-safe-mode-under-vista.md)
</dt> </dl>

 

 
