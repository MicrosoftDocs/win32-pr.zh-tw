---
description: 主控台專案是可讓使用者設定 Windows 環境的 Dll 或可執行檔 ( .exe) 檔。 通常您可以按一下主控台中的圖示來存取它們。
title: 執行主控台專案
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 2e61cbc0-fbb5-4680-8123-f8ffdcf98210
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 310d01f07d40cef69c6be30231bbf4780a1d8838
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972056"
---
# <a name="implementing-control-panel-items"></a><span data-ttu-id="651c8-104">執行主控台專案</span><span class="sxs-lookup"><span data-stu-id="651c8-104">Implementing Control Panel Items</span></span>

<span data-ttu-id="651c8-105">主控台專案是可讓使用者設定 Windows 環境的 Dll 或可執行檔 ( .exe) 檔。</span><span class="sxs-lookup"><span data-stu-id="651c8-105">Control Panel items are DLLs or executable (.exe) files that let users configure the environment of Windows.</span></span> <span data-ttu-id="651c8-106">通常您可以按一下主控台中的圖示來存取它們。</span><span class="sxs-lookup"><span data-stu-id="651c8-106">They are typically accessed by clicking an icon in the Control Panel.</span></span>

<span data-ttu-id="651c8-107">本節說明主控台專案，並說明如何建立及註冊它們，以便在主控台中適當地顯示。</span><span class="sxs-lookup"><span data-stu-id="651c8-107">This section describes Control Panel items and explains how to create and register them so that they appear appropriately in the Control Panel.</span></span> <span data-ttu-id="651c8-108">在 Windows Vista 中，會包含資訊，告訴您如何新增出現在主控台專案下以及主控台搜尋結果中的工作連結。</span><span class="sxs-lookup"><span data-stu-id="651c8-108">For Windows Vista, information is included that tells you how to add task links that appear under the Control Panel item and in Control Panel search results.</span></span>

-   [<span data-ttu-id="651c8-109">使用者體驗指南</span><span class="sxs-lookup"><span data-stu-id="651c8-109">User Experience Guidelines</span></span>](user-experience-guidelines.md)
-   [<span data-ttu-id="651c8-110">註冊主控台專案</span><span class="sxs-lookup"><span data-stu-id="651c8-110">Registering Control Panel Items</span></span>](registering-control-panel-items.md)
-   [<span data-ttu-id="651c8-111">如何註冊可執行檔主控台專案</span><span class="sxs-lookup"><span data-stu-id="651c8-111">How To Register Executable Control Panel Items</span></span>](how-to-register-an-executable-control-panel-item-registration-.md)
-   [<span data-ttu-id="651c8-112">如何註冊 DLL 主控台專案</span><span class="sxs-lookup"><span data-stu-id="651c8-112">How To Register DLL Control Panel Items</span></span>](how-to-register-dll-control-panel-item-registration-.md)
-   [<span data-ttu-id="651c8-113">使用 CPLApplet</span><span class="sxs-lookup"><span data-stu-id="651c8-113">Using CPLApplet</span></span>](using-cplapplet.md)
-   [<span data-ttu-id="651c8-114">主控台訊息處理</span><span class="sxs-lookup"><span data-stu-id="651c8-114">Control Panel Message Processing</span></span>](message-processing.md)
-   [<span data-ttu-id="651c8-115">執行主控台專案</span><span class="sxs-lookup"><span data-stu-id="651c8-115">Executing Control Panel Items</span></span>](executing-control-panel-items.md)
-   [<span data-ttu-id="651c8-116">擴充系統主控台專案</span><span class="sxs-lookup"><span data-stu-id="651c8-116">Extending System Control Panel Items</span></span>](extending-system-control-panel-items.md)
-   [<span data-ttu-id="651c8-117">指派主控台分類</span><span class="sxs-lookup"><span data-stu-id="651c8-117">Assigning Control Panel Categories</span></span>](assigning-control-panel-categories.md)
-   [<span data-ttu-id="651c8-118">建立主控台專案的可搜尋工作連結</span><span class="sxs-lookup"><span data-stu-id="651c8-118">Creating Searchable Task Links for a Control Panel Item</span></span>](creating-searchable-task-links.md)
-   [<span data-ttu-id="651c8-119">以安全模式存取主控台</span><span class="sxs-lookup"><span data-stu-id="651c8-119">Accessing the Control Panel in Safe Mode</span></span>](accessing-the-cp-in-safe-mode-under-vista.md)
-   [<span data-ttu-id="651c8-120">主控台專案的正式名稱</span><span class="sxs-lookup"><span data-stu-id="651c8-120">Canonical Names of Control Panel Items</span></span>](controlpanel-canonical-names.md)

 

 



