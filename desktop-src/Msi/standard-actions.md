---
description: 動作會封裝在安裝或維護應用程式期間執行的一般功能。 Windows Installer 有許多內建的標準動作。 安裝套件的開發人員也可以撰寫自己的自訂動作。
ms.assetid: 33651988-e371-4258-96a7-bcd7d6762161
title: 標準動作
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48ed4f9c2a7fc6671442f6b72cd10889e2fcf5e9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104192306"
---
# <a name="standard-actions"></a><span data-ttu-id="b8db7-105">標準動作</span><span class="sxs-lookup"><span data-stu-id="b8db7-105">Standard Actions</span></span>

<span data-ttu-id="b8db7-106">動作會封裝在安裝或維護應用程式期間執行的一般功能。</span><span class="sxs-lookup"><span data-stu-id="b8db7-106">An action encapsulates a typical function performed during the installation or maintenance of an application.</span></span> <span data-ttu-id="b8db7-107">Windows Installer 有許多內建的標準動作。</span><span class="sxs-lookup"><span data-stu-id="b8db7-107">Windows Installer has many built-in standard actions.</span></span> <span data-ttu-id="b8db7-108">安裝套件的開發人員也可以撰寫自己的 [自訂動作](custom-actions.md)。</span><span class="sxs-lookup"><span data-stu-id="b8db7-108">Developers of installation packages can also author their own [custom actions](custom-actions.md).</span></span>

<span data-ttu-id="b8db7-109">安裝程式標準動作的範例包括：</span><span class="sxs-lookup"><span data-stu-id="b8db7-109">Examples of installer standard actions include:</span></span>

-   <span data-ttu-id="b8db7-110">[CreateShortcuts 動作](createshortcuts-action.md)：管理與目前應用程式一起安裝之檔案的快捷方式建立。</span><span class="sxs-lookup"><span data-stu-id="b8db7-110">[CreateShortcuts action](createshortcuts-action.md): Manages the creation of shortcuts to files installed with the current application.</span></span> <span data-ttu-id="b8db7-111">此動作會使用 [快速鍵表格](shortcut-table.md) 來取得其資料。</span><span class="sxs-lookup"><span data-stu-id="b8db7-111">This action uses the [Shortcut table](shortcut-table.md) for its data.</span></span>
-   <span data-ttu-id="b8db7-112">[InstallFiles 動作](installfiles-action.md)：將選取的檔案從來源目錄複寫到目的地目錄。</span><span class="sxs-lookup"><span data-stu-id="b8db7-112">[InstallFiles action](installfiles-action.md): Copies selected files from the source directory to the destination directory.</span></span> <span data-ttu-id="b8db7-113">此動作會使用 [File 資料表](file-table.md) 來取得其資料。</span><span class="sxs-lookup"><span data-stu-id="b8db7-113">This action uses the [File table](file-table.md) for its data.</span></span>
-   <span data-ttu-id="b8db7-114">[WriteRegistryValues 動作](writeregistryvalues-action.md)：設定應用程式在登錄中所需的登錄資訊。</span><span class="sxs-lookup"><span data-stu-id="b8db7-114">[WriteRegistryValues action](writeregistryvalues-action.md): Sets up registry information the application requires in the registry.</span></span> <span data-ttu-id="b8db7-115">此動作會使用登錄 [資料表](registry-table.md) 來取得其資料。</span><span class="sxs-lookup"><span data-stu-id="b8db7-115">This action uses the [Registry table](registry-table.md) for its data.</span></span>

<span data-ttu-id="b8db7-116">下列各節將討論標準動作。</span><span class="sxs-lookup"><span data-stu-id="b8db7-116">The following sections discuss standard actions.</span></span>

-   [<span data-ttu-id="b8db7-117">關於標準動作</span><span class="sxs-lookup"><span data-stu-id="b8db7-117">About Standard Actions</span></span>](about-standard-actions.md)
-   [<span data-ttu-id="b8db7-118">使用標準動作</span><span class="sxs-lookup"><span data-stu-id="b8db7-118">Using Standard Actions</span></span>](using-standard-actions.md)
-   [<span data-ttu-id="b8db7-119">標準動作參考</span><span class="sxs-lookup"><span data-stu-id="b8db7-119">Standard Actions Reference</span></span>](standard-actions-reference.md)

 

 



