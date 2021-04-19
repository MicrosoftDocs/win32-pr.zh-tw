---
description: 遵循這些指導方針，以促進 Windows Installer 套件的當地語系化。
ms.assetid: f00b44b4-e8ec-46d2-b329-00728a83275b
title: 準備 Windows Installer 套件以進行當地語系化
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa46af5259b880398aa84dc817eb201bd63456eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972160"
---
# <a name="preparing-a-windows-installer-package-for-localization"></a><span data-ttu-id="cd7c0-103">準備 Windows Installer 套件以進行當地語系化</span><span class="sxs-lookup"><span data-stu-id="cd7c0-103">Preparing a Windows Installer Package for Localization</span></span>

<span data-ttu-id="cd7c0-104">您可以執行下列動作，以大幅促成將 Windows Installer 封裝當地語系化為多種語言：</span><span class="sxs-lookup"><span data-stu-id="cd7c0-104">Localization of a Windows Installer package into multiple languages can be greatly facilitated by doing the following:</span></span>

-   <span data-ttu-id="cd7c0-105">撰寫以字碼頁中立的基礎安裝資料庫。</span><span class="sxs-lookup"><span data-stu-id="cd7c0-105">Author a base installation database that is code page neutral.</span></span> <span data-ttu-id="cd7c0-106">請參閱 [使用中性程式碼建立資料庫頁面](creating-a-database-with-a-neutral-code-page.md)。</span><span class="sxs-lookup"><span data-stu-id="cd7c0-106">See [Creating a database with a neutral code page](creating-a-database-with-a-neutral-code-page.md).</span></span> <span data-ttu-id="cd7c0-107">然後，您可以將具有非中性字碼頁的文字保存資料表匯入至基底資料庫，以設定當地語系化資料庫的字碼頁。</span><span class="sxs-lookup"><span data-stu-id="cd7c0-107">The code page of the localized database can then be set by importing a text archive table with a non-neutral code page into the base database.</span></span> <span data-ttu-id="cd7c0-108">請參閱 [設定資料庫的字碼頁](setting-the-code-page-of-a-database.md)。</span><span class="sxs-lookup"><span data-stu-id="cd7c0-108">See [Setting the code page of a database](setting-the-code-page-of-a-database.md).</span></span>
-   <span data-ttu-id="cd7c0-109">將需要當地語系化的檔案組織成個別的元件，並將這些檔案安裝在不同的目錄中。</span><span class="sxs-lookup"><span data-stu-id="cd7c0-109">Organize files requiring localization into separate components and install these files into separate directories.</span></span> <span data-ttu-id="cd7c0-110">這可確保兩個當地語系化的封裝永遠不會在相同的目錄中安裝相同的命名檔案。</span><span class="sxs-lookup"><span data-stu-id="cd7c0-110">This ensures that two localized packages never install identically named files into the same directory.</span></span>

<span data-ttu-id="cd7c0-111">例如，使用下列資源的全球應用程式可能會有三個元件。</span><span class="sxs-lookup"><span data-stu-id="cd7c0-111">For example, a worldwide application using the following resources may have three components.</span></span>



| <span data-ttu-id="cd7c0-112">元件</span><span class="sxs-lookup"><span data-stu-id="cd7c0-112">Component</span></span> | <span data-ttu-id="cd7c0-113">資源</span><span class="sxs-lookup"><span data-stu-id="cd7c0-113">Resource</span></span>                   |
|-----------|----------------------------|
| <span data-ttu-id="cd7c0-114">世界</span><span class="sxs-lookup"><span data-stu-id="cd7c0-114">WORLD</span></span>     | <span data-ttu-id="cd7c0-115">worldwide.exe</span><span class="sxs-lookup"><span data-stu-id="cd7c0-115">worldwide.exe</span></span>              |
| <span data-ttu-id="cd7c0-116">世界</span><span class="sxs-lookup"><span data-stu-id="cd7c0-116">WORLD</span></span>     | <span data-ttu-id="cd7c0-117">全球登錄專案</span><span class="sxs-lookup"><span data-stu-id="cd7c0-117">worldwide registry entries</span></span> |
| <span data-ttu-id="cd7c0-118">世界</span><span class="sxs-lookup"><span data-stu-id="cd7c0-118">WORLD</span></span>     | <span data-ttu-id="cd7c0-119">全球快速鍵</span><span class="sxs-lookup"><span data-stu-id="cd7c0-119">worldwide shortcut</span></span>         |
| <span data-ttu-id="cd7c0-120">ENG</span><span class="sxs-lookup"><span data-stu-id="cd7c0-120">ENG</span></span>       | <span data-ttu-id="cd7c0-121">engui.dll</span><span class="sxs-lookup"><span data-stu-id="cd7c0-121">engui.dll</span></span>                  |
| <span data-ttu-id="cd7c0-122">ENG</span><span class="sxs-lookup"><span data-stu-id="cd7c0-122">ENG</span></span>       | <span data-ttu-id="cd7c0-123">readme.txt</span><span class="sxs-lookup"><span data-stu-id="cd7c0-123">readme.txt</span></span>                 |
| <span data-ttu-id="cd7c0-124">FRA</span><span class="sxs-lookup"><span data-stu-id="cd7c0-124">FRA</span></span>       | <span data-ttu-id="cd7c0-125">fraui.dll</span><span class="sxs-lookup"><span data-stu-id="cd7c0-125">fraui.dll</span></span>                  |
| <span data-ttu-id="cd7c0-126">FRA</span><span class="sxs-lookup"><span data-stu-id="cd7c0-126">FRA</span></span>       | <span data-ttu-id="cd7c0-127">readme.txt</span><span class="sxs-lookup"><span data-stu-id="cd7c0-127">readme.txt</span></span>                 |



 

<span data-ttu-id="cd7c0-128">需要當地語系化的檔案可能會安裝到下列目錄位置：</span><span class="sxs-lookup"><span data-stu-id="cd7c0-128">The files that need to be localized may be installed into the following directory locations:</span></span>

-   <span data-ttu-id="cd7c0-129">\[ProgramFilesFolder \] \\ World \\worldwide.exe</span><span class="sxs-lookup"><span data-stu-id="cd7c0-129">\[ProgramFilesFolder\]\\World\\worldwide.exe</span></span>
-   <span data-ttu-id="cd7c0-130">\[ProgramFilesFolder \] \\ World \\ 英文 \\engui.dll</span><span class="sxs-lookup"><span data-stu-id="cd7c0-130">\[ProgramFilesFolder\]\\World\\English\\engui.dll</span></span>
-   <span data-ttu-id="cd7c0-131">\[ProgramFilesFolder \] \\ World \\ 英文 \\readme.txt</span><span class="sxs-lookup"><span data-stu-id="cd7c0-131">\[ProgramFilesFolder\]\\World\\English\\readme.txt</span></span>
-   <span data-ttu-id="cd7c0-132">\[ProgramFilesFolder \] \\ World \\ 法文 \\fraui.dll</span><span class="sxs-lookup"><span data-stu-id="cd7c0-132">\[ProgramFilesFolder\]\\World\\French\\fraui.dll</span></span>
-   <span data-ttu-id="cd7c0-133">\[ProgramFilesFolder \] \\ World \\ 法文 \\readme.txt</span><span class="sxs-lookup"><span data-stu-id="cd7c0-133">\[ProgramFilesFolder\]\\World\\French\\readme.txt</span></span>

 

 



