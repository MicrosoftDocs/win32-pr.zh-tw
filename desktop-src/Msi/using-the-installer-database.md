---
description: 安裝程式資料庫可讓安裝封裝的開發人員控制將應用程式從來源傳送到目標映射的程式。
ms.assetid: 058cefcd-83dd-4a13-bd55-11d52f9d41f5
title: 使用安裝程式資料庫
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb22b9c66547c849b4c9cbd012e78b22d9301756
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106976909"
---
# <a name="using-the-installer-database"></a><span data-ttu-id="d4e49-103">使用安裝程式資料庫</span><span class="sxs-lookup"><span data-stu-id="d4e49-103">Using the Installer Database</span></span>

<span data-ttu-id="d4e49-104">安裝 [程式資料庫](installer-database.md) 可讓安裝封裝的開發人員控制將應用程式從來源傳送到目標映射的程式。</span><span class="sxs-lookup"><span data-stu-id="d4e49-104">The [Installer Database](installer-database.md) enables the developer of an installation package to control the transfer of an application from a source to a target image.</span></span> <span data-ttu-id="d4e49-105">應用程式的來源和目標影像的版面配置都是在 [目錄](directory-table.md) 資料表中指定的，而安裝應用程式的動作則是以六個順序表格來指定：</span><span class="sxs-lookup"><span data-stu-id="d4e49-105">The layout of both the source and target images of the application are specified in the [Directory](directory-table.md) table and the actions that install the application are specified in six sequence tables:</span></span>

-   <span data-ttu-id="d4e49-106">[InstallUISequence](installuisequence-table.md) 資料表</span><span class="sxs-lookup"><span data-stu-id="d4e49-106">[InstallUISequence](installuisequence-table.md) table</span></span>
-   <span data-ttu-id="d4e49-107">[InstallExecuteSequence](installexecutesequence-table.md) 資料表</span><span class="sxs-lookup"><span data-stu-id="d4e49-107">[InstallExecuteSequence](installexecutesequence-table.md) table</span></span>
-   <span data-ttu-id="d4e49-108">[AdminUISequence](adminuisequence-table.md) 資料表</span><span class="sxs-lookup"><span data-stu-id="d4e49-108">[AdminUISequence](adminuisequence-table.md) table</span></span>
-   <span data-ttu-id="d4e49-109">[AdminExecuteSequence](adminexecutesequence-table.md) 資料表</span><span class="sxs-lookup"><span data-stu-id="d4e49-109">[AdminExecuteSequence](adminexecutesequence-table.md) table</span></span>
-   <span data-ttu-id="d4e49-110">[AdvtUISequence](advtuisequence-table.md) 資料表</span><span class="sxs-lookup"><span data-stu-id="d4e49-110">[AdvtUISequence](advtuisequence-table.md) table</span></span>
-   <span data-ttu-id="d4e49-111">[AdvtExecuteSequence](advtexecutesequence-table.md) 資料表</span><span class="sxs-lookup"><span data-stu-id="d4e49-111">[AdvtExecuteSequence](advtexecutesequence-table.md) table</span></span>

<span data-ttu-id="d4e49-112">下列各節說明如何使用 [安裝程式資料庫](installer-database.md)：</span><span class="sxs-lookup"><span data-stu-id="d4e49-112">The following sections describe how to use the [Installer Database](installer-database.md):</span></span>

-   [<span data-ttu-id="d4e49-113">使用目錄資料表</span><span class="sxs-lookup"><span data-stu-id="d4e49-113">Using the Directory Table</span></span>](using-the-directory-table.md)
-   [<span data-ttu-id="d4e49-114">使用順序資料表</span><span class="sxs-lookup"><span data-stu-id="d4e49-114">Using a Sequence Table</span></span>](using-a-sequence-table.md)
-   [<span data-ttu-id="d4e49-115">取得資料庫控制碼</span><span class="sxs-lookup"><span data-stu-id="d4e49-115">Obtaining a Database Handle</span></span>](obtaining-a-database-handle.md)
-   [<span data-ttu-id="d4e49-116">認可資料庫</span><span class="sxs-lookup"><span data-stu-id="d4e49-116">Committing Databases</span></span>](committing-databases.md)
-   [<span data-ttu-id="d4e49-117">匯入和匯出</span><span class="sxs-lookup"><span data-stu-id="d4e49-117">Importing and Exporting</span></span>](importing-and-exporting.md)
-   [<span data-ttu-id="d4e49-118">合併資料庫</span><span class="sxs-lookup"><span data-stu-id="d4e49-118">Merging Databases</span></span>](merging-databases.md)
-   [<span data-ttu-id="d4e49-119">命名自訂資料表、屬性和動作</span><span class="sxs-lookup"><span data-stu-id="d4e49-119">Naming Custom Tables, Properties, and Actions</span></span>](naming-custom-tables-properties-and-actions.md)
-   [<span data-ttu-id="d4e49-120">資料流程的 OLE 限制</span><span class="sxs-lookup"><span data-stu-id="d4e49-120">OLE Limitations on Streams</span></span>](ole-limitations-on-streams.md)
-   [<span data-ttu-id="d4e49-121">使用查詢</span><span class="sxs-lookup"><span data-stu-id="d4e49-121">Working with Queries</span></span>](working-with-queries.md)
-   [<span data-ttu-id="d4e49-122">使用 SQL 將二進位資料新增至資料表</span><span class="sxs-lookup"><span data-stu-id="d4e49-122">Adding Binary Data to a Table Using SQL</span></span>](adding-binary-data-to-a-table-using-sql.md)
-   [<span data-ttu-id="d4e49-123">使用記錄</span><span class="sxs-lookup"><span data-stu-id="d4e49-123">Working with Records</span></span>](working-with-records.md)
-   [<span data-ttu-id="d4e49-124">使用資料夾位置</span><span class="sxs-lookup"><span data-stu-id="d4e49-124">Working with Folder Locations</span></span>](working-with-folder-locations.md)
-   [<span data-ttu-id="d4e49-125">指定自我註冊的順序</span><span class="sxs-lookup"><span data-stu-id="d4e49-125">Specifying the Order of Self Registration</span></span>](specifying-the-order-of-self-registration.md)
-   [<span data-ttu-id="d4e49-126">要在移除期間執行的調節動作</span><span class="sxs-lookup"><span data-stu-id="d4e49-126">Conditioning Actions to Run During Removal</span></span>](conditioning-actions-to-run-during-removal.md)
-   [<span data-ttu-id="d4e49-127">從程式呼叫資料庫函式</span><span class="sxs-lookup"><span data-stu-id="d4e49-127">Calling Database Functions from Programs</span></span>](calling-database-functions-from-programs.md)
-   [<span data-ttu-id="d4e49-128">條件陳述式語法</span><span class="sxs-lookup"><span data-stu-id="d4e49-128">Conditional Statement Syntax</span></span>](conditional-statement-syntax.md)
-   [<span data-ttu-id="d4e49-129">資料行定義格式</span><span class="sxs-lookup"><span data-stu-id="d4e49-129">Column Definition Format</span></span>](column-definition-format.md)
-   [<span data-ttu-id="d4e49-130">判斷資料行是否為主要或外部索引鍵</span><span class="sxs-lookup"><span data-stu-id="d4e49-130">Determining Whether a Column is a Primary or External Key</span></span>](determining-whether-a-column-is-a-primary-or-external-key.md)

 

 



