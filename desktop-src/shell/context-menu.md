---
description: 本節將討論如何建立快捷方式 (內容) 功能表，以及如何 (動詞) 處理常式來執行快捷方式功能表。
title: 快捷方式 (內容) 功能表和快捷方式功能表處理常式
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 956f3b10-2bc6-4f1f-a6ed-7184f94b545a
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 286dd9c860ae79e5124439439da97f206b4aa436
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191181"
---
# <a name="shortcut-context-menus-and-shortcut-menu-handlers"></a><span data-ttu-id="86541-103">快捷方式 (內容) 功能表和快捷方式功能表處理常式</span><span class="sxs-lookup"><span data-stu-id="86541-103">Shortcut (Context) Menus and Shortcut Menu Handlers</span></span>

<span data-ttu-id="86541-104">本節將討論如何建立快捷方式 (內容) 功能表，以及如何 (動詞) 處理常式來執行快捷方式功能表。</span><span class="sxs-lookup"><span data-stu-id="86541-104">This section discusses the creation of shortcut (context) menus, and the implementation of shortcut menu (verb) handlers.</span></span>

<span data-ttu-id="86541-105">這一節的檔案類型和檔案關聯的組織方式如下：</span><span class="sxs-lookup"><span data-stu-id="86541-105">This section on file types and file associations is organized as follows:</span></span>

-   [<span data-ttu-id="86541-106">動詞和檔案關聯</span><span class="sxs-lookup"><span data-stu-id="86541-106">Verbs and File Associations</span></span>](fa-verbs.md)
-   [<span data-ttu-id="86541-107">選擇靜態或動態快捷方式功能表方法</span><span class="sxs-lookup"><span data-stu-id="86541-107">Choosing a Static or Dynamic Shortcut Menu Method</span></span>](shortcut-choose-method.md)
-   [<span data-ttu-id="86541-108">快速鍵功能表處理常式和多個動詞的最佳作法</span><span class="sxs-lookup"><span data-stu-id="86541-108">Best Practices for Shortcut Menu Handlers and Multiple Verbs</span></span>](verbs-best-practices.md)
-   [<span data-ttu-id="86541-109">建立快捷方式功能表處理常式</span><span class="sxs-lookup"><span data-stu-id="86541-109">Creating Shortcut Menu Handlers</span></span>](context-menu-handlers.md)
-   [<span data-ttu-id="86541-110">建立靜態串聯功能表</span><span class="sxs-lookup"><span data-stu-id="86541-110">Creating Static Cascading Menus</span></span>](creating-static-cascading-menus.md)
-   [<span data-ttu-id="86541-111">如何隱藏和控制動詞可見度</span><span class="sxs-lookup"><span data-stu-id="86541-111">How to Suppress and Control Verb Visibility</span></span>](how-to-suppress-and-control-visibility.md)
-   [<span data-ttu-id="86541-112">如何使用動詞選取模型</span><span class="sxs-lookup"><span data-stu-id="86541-112">How to Employ the Verb Selection Model</span></span>](how-to-employ-the-verb-selection-model.md)
-   [<span data-ttu-id="86541-113">如何使用專案屬性</span><span class="sxs-lookup"><span data-stu-id="86541-113">How to Use Item Attributes</span></span>](how-to-use-item-attributes.md)
-   [<span data-ttu-id="86541-114">如何透過 Desktop.ini為資料夾執行自訂動詞 </span><span class="sxs-lookup"><span data-stu-id="86541-114">How to Implement Custom Verbs for Folders through Desktop.ini</span></span>](how-to-implement-custom-verbs-for-folders-through-desktop-ini.md)
-   [<span data-ttu-id="86541-115">使用動態動詞自訂快捷方式功能表</span><span class="sxs-lookup"><span data-stu-id="86541-115">Customizing a Shortcut Menu Using Dynamic Verbs</span></span>](shortcut-menu-using-dynamic-verbs.md)
-   [<span data-ttu-id="86541-116">如何執行 ICoNtextMenu 介面</span><span class="sxs-lookup"><span data-stu-id="86541-116">How to Implement the IContextMenu Interface</span></span>](how-to-implement-the-icontextmenu-interface.md)
-   [<span data-ttu-id="86541-117">快速鍵功能表參考</span><span class="sxs-lookup"><span data-stu-id="86541-117">Shortcut Menu Reference</span></span>](context-menu-reference.md)

## <a name="additional-resources"></a><span data-ttu-id="86541-118">其他資源</span><span class="sxs-lookup"><span data-stu-id="86541-118">Additional Resources</span></span>

<span data-ttu-id="86541-119">如需相關的概念背景，請參閱下列主題：</span><span class="sxs-lookup"><span data-stu-id="86541-119">For related conceptual background, see the following topics:</span></span>

-   <span data-ttu-id="86541-120">檔案[關聯簡介](fa-intro.md)。</span><span class="sxs-lookup"><span data-stu-id="86541-120">[Introduction to File Associations](fa-intro.md).</span></span>
-   <span data-ttu-id="86541-121">若要使用檔案類型處理常式來擴充 Shell，請參閱 [建立 Shell 擴充處理常式](handlers.md)。</span><span class="sxs-lookup"><span data-stu-id="86541-121">To extend the Shell with file type handlers, see [Creating Shell Extension Handlers](handlers.md).</span></span>
-   <span data-ttu-id="86541-122">若要建立 Shell 資料存放區，請參閱 [執行基本資料夾物件介面](nse-implement.md)。</span><span class="sxs-lookup"><span data-stu-id="86541-122">To create a Shell data store, see [Implementing the Basic Folder Object Interfaces](nse-implement.md).</span></span>

<span data-ttu-id="86541-123">如需相關的參考檔，請參閱下列主題：</span><span class="sxs-lookup"><span data-stu-id="86541-123">For related reference documenation, see the following topics:</span></span>

-   <span data-ttu-id="86541-124">若要在 Shell 專案上執行動詞命令，請參閱 [**InvokeVerb**](folderitem-invokeverb.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="86541-124">To execute a verb on a Shell item, see the [**InvokeVerb**](folderitem-invokeverb.md) method.</span></span>
-   <span data-ttu-id="86541-125">若要取得可在 Shell 專案上執行的動詞集合，請參閱 [**動詞**](folderitem-verbs.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="86541-125">To retrieve a collection of verbs that can be executed on a Shell item, see the [**Verbs**](folderitem-verbs.md) method.</span></span>
-   <span data-ttu-id="86541-126">若要在指定的檔案上執行作業，請參閱 [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea) 或 [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) 函數。</span><span class="sxs-lookup"><span data-stu-id="86541-126">To perform an operation on a specified file, see either the [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea) or [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) functions.</span></span>

 

 



