---
description: 瞭解如何延伸 Windows 檔案總管功能區。
title: 擴充功能區
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 0C043FF8-3862-4F02-8700-BB556C4F35B8
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 6a0a3af3ac21e0bac0471bc9a987849536303556
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104511036"
---
# <a name="extending-the-ribbon"></a><span data-ttu-id="9b95a-103">擴充功能區</span><span class="sxs-lookup"><span data-stu-id="9b95a-103">Extending the Ribbon</span></span>

<span data-ttu-id="9b95a-104">在 Windows 檔案總管中，功能區有助於讓常見的終端使用者檔案管理活動更容易且更容易探索，但應用程式開發人員也有變更比賽即將展開。</span><span class="sxs-lookup"><span data-stu-id="9b95a-104">In Windows Explorer, the Ribbon helps make common end-user file management activities easier and more discoverable, but there are changes afoot for app developers.</span></span> <span data-ttu-id="9b95a-105">例如，舊的命令列可自由擴充，但此時功能區會受到更多的限制。</span><span class="sxs-lookup"><span data-stu-id="9b95a-105">For example, the old command bar was freely extensible but the Ribbon is more restricted at this time.</span></span> <span data-ttu-id="9b95a-106">此外，所有命名空間延伸模組預設都不會顯示功能區，所以您必須選擇取得功能區;否則，您會取得較舊的命令列。</span><span class="sxs-lookup"><span data-stu-id="9b95a-106">Also, the Ribbon is not shown by default for all namespace extensions, so you have to opt in to get the Ribbon; otherwise, you get the older command bar.</span></span>

<span data-ttu-id="9b95a-107">使用者可以在功能區上使用的動作可以分為三種擴充性類別：</span><span class="sxs-lookup"><span data-stu-id="9b95a-107">Actions available to users on the Ribbon fall into three extensibility categories:</span></span>

-   <span data-ttu-id="9b95a-108">不需要擴充性。</span><span class="sxs-lookup"><span data-stu-id="9b95a-108">Extensibility is not needed.</span></span> <span data-ttu-id="9b95a-109">範例：複製、貼上、刪除。</span><span class="sxs-lookup"><span data-stu-id="9b95a-109">Examples: Copy, Paste, Delete.</span></span> <span data-ttu-id="9b95a-110">Windows 會為您處理這些動詞。</span><span class="sxs-lookup"><span data-stu-id="9b95a-110">Windows handles these verbs for you.</span></span>
-   <span data-ttu-id="9b95a-111">目前不允許擴充性：範例： Zip、Close Session 和其他自訂動作。</span><span class="sxs-lookup"><span data-stu-id="9b95a-111">Extensibility is not currently allowed: Examples: Zip, Close Session, and other custom actions.</span></span> <span data-ttu-id="9b95a-112">使用內容功能表來涵蓋這些案例。</span><span class="sxs-lookup"><span data-stu-id="9b95a-112">Use the context menu to cover these scenarios.</span></span>
-   <span data-ttu-id="9b95a-113">擴充功能內建于動作本身。</span><span class="sxs-lookup"><span data-stu-id="9b95a-113">Extensibility is built into the action itself.</span></span> <span data-ttu-id="9b95a-114">範例：搜尋、電子郵件、列印、新專案。</span><span class="sxs-lookup"><span data-stu-id="9b95a-114">Examples: Search, Email, Print, New Item.</span></span> <span data-ttu-id="9b95a-115">您必須註冊這些動詞，以將您的應用程式或檔案格式包含在功能區中。</span><span class="sxs-lookup"><span data-stu-id="9b95a-115">You need to register for these verbs to include your app or file format in the Ribbon .</span></span>

<span data-ttu-id="9b95a-116">本檔說明如何加入宣告以取得功能區，以及如何註冊來處理特定功能區動詞。</span><span class="sxs-lookup"><span data-stu-id="9b95a-116">This document describes how you can opt-in to get the Ribbon, and how to register to handle specific Ribbon verbs.</span></span>

## <a name="opting-in-to-the-ribbon"></a><span data-ttu-id="9b95a-117">加入宣告功能區</span><span class="sxs-lookup"><span data-stu-id="9b95a-117">Opting in to the Ribbon</span></span>

<span data-ttu-id="9b95a-118">若要加入宣告功能區，您的 [**IShellFolder2**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellfolder2)執行應該在 [**IExplorerPaneVisibility：： GetPaneState**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iexplorerpanevisibility-getpanestate)中指定 **EP \_ 功能區**，並在上傳回 **eps \_ 強制** \| **eps \_ 預設值 \_**。</span><span class="sxs-lookup"><span data-stu-id="9b95a-118">To opt in to the Ribbon, your [**IShellFolder2**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellfolder2) implementation should specify **EP\_Ribbon** in [**IExplorerPaneVisibility::GetPaneState**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iexplorerpanevisibility-getpanestate) and return **EPS\_FORCE** \| **EPS\_DEFAULT\_ON**.</span></span>

## <a name="extending-the-ribbon-for-file-extensions"></a><span data-ttu-id="9b95a-119">擴充副檔名的功能區</span><span class="sxs-lookup"><span data-stu-id="9b95a-119">Extending the Ribbon for File Extensions</span></span>

<span data-ttu-id="9b95a-120">這些功能區按鈕可根據副檔名進行擴充：</span><span class="sxs-lookup"><span data-stu-id="9b95a-120">These Ribbon buttons are extensible based on file extensions:</span></span>

-   <span data-ttu-id="9b95a-121">全部解壓縮</span><span class="sxs-lookup"><span data-stu-id="9b95a-121">Extract All</span></span>
-   <span data-ttu-id="9b95a-122">\| (ISO) 掛接燒錄</span><span class="sxs-lookup"><span data-stu-id="9b95a-122">Mount \| Burn (an ISO)</span></span>
-   <span data-ttu-id="9b95a-123">播放播放 \| 全部 \| 新增至播放清單 (動詞：排入佇列) </span><span class="sxs-lookup"><span data-stu-id="9b95a-123">Play \| Play All \| Add to Playlist (verb: Enqueue)</span></span>
-   <span data-ttu-id="9b95a-124">開啟</span><span class="sxs-lookup"><span data-stu-id="9b95a-124">Open</span></span>
-   <span data-ttu-id="9b95a-125">編輯</span><span class="sxs-lookup"><span data-stu-id="9b95a-125">Edit</span></span>
-   <span data-ttu-id="9b95a-126">屬性</span><span class="sxs-lookup"><span data-stu-id="9b95a-126">Properties</span></span>

<span data-ttu-id="9b95a-127">當您註冊以靜態方式處理新檔案類型的相關動詞時，功能區會適當地處理動詞。</span><span class="sxs-lookup"><span data-stu-id="9b95a-127">When you register to statically handle the relevant verbs for new file types, the Ribbon handles the verbs appropriately.</span></span> <span data-ttu-id="9b95a-128">您可以像操作功能表動詞一樣註冊。</span><span class="sxs-lookup"><span data-stu-id="9b95a-128">You register just as you would for context menu verbs.</span></span> <span data-ttu-id="9b95a-129">如需檔案關聯和註冊動詞命令的詳細資訊，請參閱 [動詞和檔案關聯](fa-verbs.md) 和 [建立快捷方式功能表處理常式](context-menu-handlers.md)。</span><span class="sxs-lookup"><span data-stu-id="9b95a-129">For more information about file associations and registering for verbs, see [Verbs and File Associations](fa-verbs.md) and [Creating Shortcut Menu Handlers](context-menu-handlers.md).</span></span>

## <a name="registering-as-a-default-handler-for-actionids"></a><span data-ttu-id="9b95a-130">註冊為 ActionIds 的預設處理常式</span><span class="sxs-lookup"><span data-stu-id="9b95a-130">Registering as a Default Handler for ActionIds</span></span>

<span data-ttu-id="9b95a-131">首先，在適當的 AssocActionId 子機碼下註冊您的 ProgId。</span><span class="sxs-lookup"><span data-stu-id="9b95a-131">First, register your ProgId under the appropriate AssocActionId subkey.</span></span> <span data-ttu-id="9b95a-132">每個 AssocActionId 子機碼代表使用者可以從功能區叫用的動詞或動作。</span><span class="sxs-lookup"><span data-stu-id="9b95a-132">Each AssocActionId subkey represents a verb or action that users can invoke from the Ribbon.</span></span> <span data-ttu-id="9b95a-133">在此範例中，應用程式會註冊 ZipSelection ActionID，以擴充功能區上的 [全部解壓縮] 按鈕。</span><span class="sxs-lookup"><span data-stu-id="9b95a-133">In this example, the app registers for the ZipSelection ActionID to extend the "Extract All" button on the Ribbon.</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Classes
         Explorer.AssocActionId.ZipSelection
            shell
               open
                  command
                     (Default) = %SystemRoot%\[Your App].exe
      Microsoft
         Windows
            CurrentVersion
               Your App Name
                  Capabilities
                     URL Protocol
                     FriendlyTypeName = @%SystemRoot%\explorer.exe,-1234
```

<span data-ttu-id="9b95a-134">註冊完成之後，您必須接著註冊來處理通訊協定，就像平常一樣，如 [預設程式](default-programs.md)中所述。</span><span class="sxs-lookup"><span data-stu-id="9b95a-134">Once that registration is complete, you must then register to handle protocols just as you normally would, as described in [Default Programs](default-programs.md).</span></span>

 

 



