---
description: Windows Installer 開發人員 Windows SDK 元件中提供了 VBScript 檔案 WiSubStg.vbs。
ms.assetid: a0248dfb-e406-4ce6-ab11-1e428aa67af4
title: 管理 Substorages
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01876efdb85bdc89df1b4d64332d44674e5e860e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320567"
---
# <a name="manage-substorages"></a><span data-ttu-id="6e611-103">管理 Substorages</span><span class="sxs-lookup"><span data-stu-id="6e611-103">Manage Substorages</span></span>

<span data-ttu-id="6e611-104">[Windows Installer 開發人員 Windows SDK 元件](platform-sdk-components-for-windows-installer-developers.md)中提供了 VBScript 檔案 WiSubStg.vbs。</span><span class="sxs-lookup"><span data-stu-id="6e611-104">The VBScript file WiSubStg.vbs is provided in the [Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).</span></span> <span data-ttu-id="6e611-105">這個範例會示範如何使用腳本來管理 Windows Installer 資料庫中的 substorages。</span><span class="sxs-lookup"><span data-stu-id="6e611-105">This sample shows how script can be used to manage substorages in a Windows Installer database.</span></span> <span data-ttu-id="6e611-106">轉換可以新增至現有的 Windows Installer 資料庫做為 substorage。</span><span class="sxs-lookup"><span data-stu-id="6e611-106">A transform can be added to an existing Windows Installer database as a substorage.</span></span>

<span data-ttu-id="6e611-107">此範例將示範如何使用：</span><span class="sxs-lookup"><span data-stu-id="6e611-107">The sample demonstrates the use of:</span></span>

-   [<span data-ttu-id="6e611-108">\_儲存體資料表</span><span class="sxs-lookup"><span data-stu-id="6e611-108">\_Storages table</span></span>](-storages-table.md)
-   [<span data-ttu-id="6e611-109">**(安裝程式物件) 的 OpenDatabase 方法**</span><span class="sxs-lookup"><span data-stu-id="6e611-109">**OpenDatabase method (Installer Object)**</span></span>](installer-opendatabase.md)
-   [<span data-ttu-id="6e611-110">**CreateRecord 方法**</span><span class="sxs-lookup"><span data-stu-id="6e611-110">**CreateRecord method**</span></span>](installer-createrecord.md)
-   <span data-ttu-id="6e611-111">[](installer-lasterrorrecord.md) [**安裝程式物件** 的 LastErrorRecord 方法](installer-object.md)</span><span class="sxs-lookup"><span data-stu-id="6e611-111">[**LastErrorRecord method**](installer-lasterrorrecord.md) of the [**Installer object**](installer-object.md)</span></span>
-   [<span data-ttu-id="6e611-112">**OpenView 方法**</span><span class="sxs-lookup"><span data-stu-id="6e611-112">**OpenView method**</span></span>](database-openview.md)
-   <span data-ttu-id="6e611-113">[](database-commit.md) [ **Database 物件** 的 Commit 方法](database-object.md)</span><span class="sxs-lookup"><span data-stu-id="6e611-113">[**Commit method**](database-commit.md) of the [**Database object**](database-object.md)</span></span>
-   [<span data-ttu-id="6e611-114">**Fetch 方法**</span><span class="sxs-lookup"><span data-stu-id="6e611-114">**Fetch method**</span></span>](view-fetch.md)
-   [<span data-ttu-id="6e611-115">**Modify 方法**</span><span class="sxs-lookup"><span data-stu-id="6e611-115">**Modify method**</span></span>](view-modify.md)
-   <span data-ttu-id="6e611-116">[](view-execute.md) [ **View 物件** 的 Execute 方法](view-object.md)</span><span class="sxs-lookup"><span data-stu-id="6e611-116">[**Execute method**](view-execute.md) of the [**View object**](view-object.md)</span></span>
-   [<span data-ttu-id="6e611-117">**至 convertfrom-stringdata 屬性**</span><span class="sxs-lookup"><span data-stu-id="6e611-117">**StringData property**</span></span>](record-stringdata.md)
-   <span data-ttu-id="6e611-118">[](record-setstream.md) [ **Record 物件** 的 SetStream 方法](record-object.md)</span><span class="sxs-lookup"><span data-stu-id="6e611-118">[**SetStream method**](record-setstream.md) of the [**Record object**](record-object.md)</span></span>

<span data-ttu-id="6e611-119">您將需要 CScript.exe 或 WScript.exe 版本的 Windows Script Host 才能使用此範例。</span><span class="sxs-lookup"><span data-stu-id="6e611-119">You'll require the CScript.exe or WScript.exe version of Windows Script Host to use this sample.</span></span> <span data-ttu-id="6e611-120">若要使用 CScript.exe 執行此範例，請使用下列語法在命令提示字元中輸入命令列。</span><span class="sxs-lookup"><span data-stu-id="6e611-120">To use CScript.exe to run this sample, type a command line at the command prompt using the following syntax.</span></span> <span data-ttu-id="6e611-121">如果第一個引數是/？，則會顯示說明</span><span class="sxs-lookup"><span data-stu-id="6e611-121">Help is displayed if the first argument is /?</span></span> <span data-ttu-id="6e611-122">或者，如果指定的引數太少。</span><span class="sxs-lookup"><span data-stu-id="6e611-122">or if too few arguments are specified.</span></span> <span data-ttu-id="6e611-123">若要將輸出重新導向至檔案，請以 VBS > 路徑結束命令列 \[  \] 。</span><span class="sxs-lookup"><span data-stu-id="6e611-123">To redirect the output to a file, end the command line with VBS > \[*path to file*\].</span></span> <span data-ttu-id="6e611-124">此範例會傳回值0表示成功，如果叫用說明，則傳回 1; 如果腳本失敗，則傳回2。</span><span class="sxs-lookup"><span data-stu-id="6e611-124">The sample returns a value of 0 for success, 1 if help is invoked, and 2 if the script fails.</span></span>

<span data-ttu-id="6e611-125">**cscript WiSubStg.vbs \[ 路徑指向檔案 \] \[ 選項的資料庫路徑 \] \[ \] \[ substorage 名稱\]**</span><span class="sxs-lookup"><span data-stu-id="6e611-125">**cscript WiSubStg.vbs \[path to database\]\[path to file\]\[options\]\[substorage name\]**</span></span>

<span data-ttu-id="6e611-126">指定 Windows Installer 資料庫的路徑，以新增或移除 substorage。</span><span class="sxs-lookup"><span data-stu-id="6e611-126">Specify the path to the Windows Installer database to add or remove substorage.</span></span> <span data-ttu-id="6e611-127">指定要新增為 substorage 的轉換或資料庫檔案的路徑。</span><span class="sxs-lookup"><span data-stu-id="6e611-127">Specify a path to the transform or database file that is being added as substorage.</span></span> <span data-ttu-id="6e611-128">若要列出 Windows Installer 資料庫中的 substorages，請省略這個檔案的路徑。</span><span class="sxs-lookup"><span data-stu-id="6e611-128">To list the substorages in the Windows Installer database, omit the path to this file.</span></span> <span data-ttu-id="6e611-129">您可以指定選擇性的 substorage 名稱，如果省略此名稱，substorage 名稱就會預設為檔案名。</span><span class="sxs-lookup"><span data-stu-id="6e611-129">You may specify an optional substorage name, if this is omitted the substorage name defaults to the file name.</span></span>

<span data-ttu-id="6e611-130">您可以指定下列選項。</span><span class="sxs-lookup"><span data-stu-id="6e611-130">The following option may be specified.</span></span>



| <span data-ttu-id="6e611-131">選項</span><span class="sxs-lookup"><span data-stu-id="6e611-131">Option</span></span>              | <span data-ttu-id="6e611-132">Description</span><span class="sxs-lookup"><span data-stu-id="6e611-132">Description</span></span>                                                                                         |
|---------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6e611-133">未指定任何選項</span><span class="sxs-lookup"><span data-stu-id="6e611-133">no option specified</span></span> | <span data-ttu-id="6e611-134">將 substorage 新增至 Windows Installer 資料庫。</span><span class="sxs-lookup"><span data-stu-id="6e611-134">Add a substorage to the Windows Installer database.</span></span>                                                 |
| <span data-ttu-id="6e611-135">/d</span><span class="sxs-lookup"><span data-stu-id="6e611-135">/d</span></span>                  | <span data-ttu-id="6e611-136">移除 substorage。</span><span class="sxs-lookup"><span data-stu-id="6e611-136">Remove a substorage.</span></span> <span data-ttu-id="6e611-137">此選項旗標後面必須接著要移除的 substorage 名稱。</span><span class="sxs-lookup"><span data-stu-id="6e611-137">This option flag must be followed by the name of the substorage to be removed.</span></span> |



 

<span data-ttu-id="6e611-138">如需其他腳本範例，請參閱 [Windows Installer 腳本範例](windows-installer-scripting-examples.md)。</span><span class="sxs-lookup"><span data-stu-id="6e611-138">For additional scripting examples, see [Windows Installer Scripting Examples](windows-installer-scripting-examples.md).</span></span> <span data-ttu-id="6e611-139">如需不需要 Windows Script Host 的範例公用程式，請參閱 [Windows Installer 開發工具](windows-installer-development-tools.md)。</span><span class="sxs-lookup"><span data-stu-id="6e611-139">For sample utilities that do not require Windows Script Host, see [Windows Installer Development Tools](windows-installer-development-tools.md).</span></span>

<span data-ttu-id="6e611-140">請注意， [當地語系化範例](a-localization-example.md) 示範如何將 [自訂轉換內嵌為 Substorage](embedding-customization-transforms-as-substorage.md)。</span><span class="sxs-lookup"><span data-stu-id="6e611-140">Note that [A Localization Example](a-localization-example.md) demonstrates [Embedding Customization Transforms as Substorage](embedding-customization-transforms-as-substorage.md).</span></span>

 

 



