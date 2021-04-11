---
description: 安裝程式會將安裝目錄結構的相關資訊保留在目錄資料表中。
ms.assetid: 31390138-b1d0-4f0b-9304-6e7c69e6a736
title: 指定目錄結構
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80a87880921799158559e28fed2c6dde97c9a331
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848186"
---
# <a name="specifying-directory-structure"></a><span data-ttu-id="1e282-103">指定目錄結構</span><span class="sxs-lookup"><span data-stu-id="1e282-103">Specifying Directory Structure</span></span>

<span data-ttu-id="1e282-104">安裝程式會將安裝目錄結構的相關資訊保留在 [目錄資料表](directory-table.md)中。</span><span class="sxs-lookup"><span data-stu-id="1e282-104">The installer keeps information about the installation directory structure in the [Directory Table](directory-table.md).</span></span> <span data-ttu-id="1e282-105">請參閱 [核心資料表群組](core-tables-group.md)。</span><span class="sxs-lookup"><span data-stu-id="1e282-105">See the [Core Tables Group](core-tables-group.md).</span></span> <span data-ttu-id="1e282-106">在本節中，您會將「記事本」範例的目錄結構資訊新增至您在匯 [入空白資料庫](importing-a-blank-database.md)時所建立的空資料庫。</span><span class="sxs-lookup"><span data-stu-id="1e282-106">In this section you add directory structure information for the Notepad sample to the empty database you created in [Importing a Blank Database](importing-a-blank-database.md).</span></span> <span data-ttu-id="1e282-107">使用 SDK 或其他編輯器提供的資料庫編輯器 Orca，在 MNP2000.msi 中開啟目錄資料表。</span><span class="sxs-lookup"><span data-stu-id="1e282-107">Use the database editor Orca that is provided with the SDK, or another editor, to open the Directory Table in MNP2000.msi.</span></span> <span data-ttu-id="1e282-108">使用編輯器，將下列資料輸入到空白目錄資料表中。</span><span class="sxs-lookup"><span data-stu-id="1e282-108">Use the editor to enter the following data into the blank Directory table.</span></span>

[<span data-ttu-id="1e282-109">目錄資料表</span><span class="sxs-lookup"><span data-stu-id="1e282-109">Directory Table</span></span>](directory-table.md)



| <span data-ttu-id="1e282-110">目錄</span><span class="sxs-lookup"><span data-stu-id="1e282-110">Directory</span></span>                                        | <span data-ttu-id="1e282-111">目錄 \_ 父系</span><span class="sxs-lookup"><span data-stu-id="1e282-111">Directory\_Parent</span></span>                                | <span data-ttu-id="1e282-112">DefaultDir</span><span class="sxs-lookup"><span data-stu-id="1e282-112">DefaultDir</span></span>        |
|--------------------------------------------------|--------------------------------------------------|-------------------|
| [<span data-ttu-id="1e282-113">**TARGETDIR**</span><span class="sxs-lookup"><span data-stu-id="1e282-113">**TARGETDIR**</span></span>](targetdir.md)                   |                                                  | <span data-ttu-id="1e282-114">SourceDir</span><span class="sxs-lookup"><span data-stu-id="1e282-114">SourceDir</span></span>         |
| [<span data-ttu-id="1e282-115">**ProgramFilesFolder**</span><span class="sxs-lookup"><span data-stu-id="1e282-115">**ProgramFilesFolder**</span></span>](programfilesfolder.md) | [<span data-ttu-id="1e282-116">**TARGETDIR**</span><span class="sxs-lookup"><span data-stu-id="1e282-116">**TARGETDIR**</span></span>](targetdir.md)                   | <span data-ttu-id="1e282-117">.</span><span class="sxs-lookup"><span data-stu-id="1e282-117">.</span></span>                 |
| <span data-ttu-id="1e282-118">ARTSDIR</span><span class="sxs-lookup"><span data-stu-id="1e282-118">ARTSDIR</span></span>                                          | <span data-ttu-id="1e282-119">NOTEPADDIR</span><span class="sxs-lookup"><span data-stu-id="1e282-119">NOTEPADDIR</span></span>                                       | <span data-ttu-id="1e282-120">藝術：活動</span><span class="sxs-lookup"><span data-stu-id="1e282-120">Arts:Events</span></span>       |
| <span data-ttu-id="1e282-121">HOLDIR</span><span class="sxs-lookup"><span data-stu-id="1e282-121">HOLDIR</span></span>                                           | <span data-ttu-id="1e282-122">MONDIR</span><span class="sxs-lookup"><span data-stu-id="1e282-122">MONDIR</span></span>                                           | <span data-ttu-id="1e282-123">.：假日</span><span class="sxs-lookup"><span data-stu-id="1e282-123">.:Holidays</span></span>        |
| <span data-ttu-id="1e282-124">MENUDIR</span><span class="sxs-lookup"><span data-stu-id="1e282-124">MENUDIR</span></span>                                          | <span data-ttu-id="1e282-125">NOTEPADDIR</span><span class="sxs-lookup"><span data-stu-id="1e282-125">NOTEPADDIR</span></span>                                       | <span data-ttu-id="1e282-126">功能表</span><span class="sxs-lookup"><span data-stu-id="1e282-126">Menu</span></span>              |
| <span data-ttu-id="1e282-127">MONDIR</span><span class="sxs-lookup"><span data-stu-id="1e282-127">MONDIR</span></span>                                           | <span data-ttu-id="1e282-128">NOTEPADDIR</span><span class="sxs-lookup"><span data-stu-id="1e282-128">NOTEPADDIR</span></span>                                       | <span data-ttu-id="1e282-129">門</span><span class="sxs-lookup"><span data-stu-id="1e282-129">Gate</span></span>              |
| <span data-ttu-id="1e282-130">NOTEPADDIR</span><span class="sxs-lookup"><span data-stu-id="1e282-130">NOTEPADDIR</span></span>                                       | [<span data-ttu-id="1e282-131">**ProgramFilesFolder**</span><span class="sxs-lookup"><span data-stu-id="1e282-131">**ProgramFilesFolder**</span></span>](programfilesfolder.md) | <span data-ttu-id="1e282-132">紅色 \_ 公園：記事本</span><span class="sxs-lookup"><span data-stu-id="1e282-132">Red\_Park:Notepad</span></span> |
| <span data-ttu-id="1e282-133">SPORTDIR</span><span class="sxs-lookup"><span data-stu-id="1e282-133">SPORTDIR</span></span>                                         | <span data-ttu-id="1e282-134">NOTEPADDIR</span><span class="sxs-lookup"><span data-stu-id="1e282-134">NOTEPADDIR</span></span>                                       | <span data-ttu-id="1e282-135">運動：活動</span><span class="sxs-lookup"><span data-stu-id="1e282-135">Sports:Events</span></span>     |



 

<span data-ttu-id="1e282-136">將此資料輸入目錄資料表中，會指定來源和目標目錄結構。</span><span class="sxs-lookup"><span data-stu-id="1e282-136">Entering this data into the Directory table specifies the source and target directory structures.</span></span> <span data-ttu-id="1e282-137">請參閱 [目錄表格](directory-table.md) ，並 [使用目錄資料表](using-the-directory-table.md) 主題。</span><span class="sxs-lookup"><span data-stu-id="1e282-137">See the [Directory Table](directory-table.md) and [Using the Directory Table](using-the-directory-table.md) topics.</span></span> <span data-ttu-id="1e282-138">請注意， [**TARGETDIR**](targetdir.md) 屬性必須是每個安裝的目錄資料表中一個根項目的名稱。</span><span class="sxs-lookup"><span data-stu-id="1e282-138">Note that the [**TARGETDIR**](targetdir.md) property must be the name of one root in the Directory table of every installation.</span></span>

[<span data-ttu-id="1e282-139">繼續</span><span class="sxs-lookup"><span data-stu-id="1e282-139">Continue</span></span>](specifying-components.md)

 

 



