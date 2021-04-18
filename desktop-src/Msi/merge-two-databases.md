---
description: Windows Installer 開發人員 Windows SDK 元件中提供了 VBScript 檔案 WiMerge.vbs。 此範例腳本會將一個 Windows Installer 資料庫合併至另一個資料庫。 如需詳細資訊，請參閱合併和轉換。
ms.assetid: 31867082-7c1d-4530-a066-236d8ee5f023
title: 合併兩個資料庫
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0254cbe2bd0785b45d4ced3a16770023e617bc63
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106971616"
---
# <a name="merge-two-databases"></a><span data-ttu-id="794b2-105">合併兩個資料庫</span><span class="sxs-lookup"><span data-stu-id="794b2-105">Merge Two Databases</span></span>

<span data-ttu-id="794b2-106">[Windows Installer 開發人員 Windows SDK 元件](platform-sdk-components-for-windows-installer-developers.md)中提供了 VBScript 檔案 WiMerge.vbs。</span><span class="sxs-lookup"><span data-stu-id="794b2-106">The VBScript file WiMerge.vbs is provided in the [Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).</span></span> <span data-ttu-id="794b2-107">此範例腳本會將一個 Windows Installer 資料庫合併至另一個資料庫。</span><span class="sxs-lookup"><span data-stu-id="794b2-107">This sample script merges one Windows Installer database into another database.</span></span> <span data-ttu-id="794b2-108">如需詳細資訊，請參閱 [合併和轉換](merges-and-transforms.md)。</span><span class="sxs-lookup"><span data-stu-id="794b2-108">For more information, see [Merges and Transforms](merges-and-transforms.md).</span></span>

<span data-ttu-id="794b2-109">[**MsiDatabaseMerge**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasemergea)函式和 [**資料庫**](database-object.md)物件的 [**merge**](database-merge.md)方法無法用來合併安裝封裝中包含的模組。</span><span class="sxs-lookup"><span data-stu-id="794b2-109">The [**MsiDatabaseMerge**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasemergea) function and the [**Merge**](database-merge.md) method of the [**Database**](database-object.md) object cannot be used to merge a module included in the installation package.</span></span> <span data-ttu-id="794b2-110">它們不應該用來將 [合併模組](merge-modules.md) 合併成 Windows Installer 套件。</span><span class="sxs-lookup"><span data-stu-id="794b2-110">They should not be used to merge [Merge Modules](merge-modules.md) into a Windows Installer package.</span></span> <span data-ttu-id="794b2-111">若要在安裝套件中包含合併模組，安裝套件的作者應遵循套用 [合併模組](applying-merge-modules.md) 主題中所述的指導方針。</span><span class="sxs-lookup"><span data-stu-id="794b2-111">To include a merge module in an installation package, authors of installation packages should follow the guidelines that are described in [Applying Merge Modules](applying-merge-modules.md) topic.</span></span>

<span data-ttu-id="794b2-112">此範例示範如何使用下列各項：</span><span class="sxs-lookup"><span data-stu-id="794b2-112">The sample demonstrates the use of the following:</span></span>

-   [<span data-ttu-id="794b2-113">**(安裝程式物件) 的 OpenDatabase 方法**</span><span class="sxs-lookup"><span data-stu-id="794b2-113">**OpenDatabase method (Installer Object)**</span></span>](installer-opendatabase.md)
-   <span data-ttu-id="794b2-114">[](installer-lasterrorrecord.md) [**安裝程式物件** 的 LastErrorRecord 方法](installer-object.md)</span><span class="sxs-lookup"><span data-stu-id="794b2-114">[**LastErrorRecord method**](installer-lasterrorrecord.md) of the [**Installer object**](installer-object.md)</span></span>
-   [<span data-ttu-id="794b2-115">**OpenView 方法**</span><span class="sxs-lookup"><span data-stu-id="794b2-115">**OpenView method**</span></span>](database-openview.md)
-   [<span data-ttu-id="794b2-116">**Merge 方法**</span><span class="sxs-lookup"><span data-stu-id="794b2-116">**Merge method**</span></span>](database-merge.md)
-   <span data-ttu-id="794b2-117">[](database-commit.md) [ **Database 物件** 的 Commit 方法](database-object.md)</span><span class="sxs-lookup"><span data-stu-id="794b2-117">[**Commit method**](database-commit.md) of the [**Database object**](database-object.md)</span></span>
-   [<span data-ttu-id="794b2-118">**Fetch 方法**</span><span class="sxs-lookup"><span data-stu-id="794b2-118">**Fetch method**</span></span>](view-fetch.md)
-   [<span data-ttu-id="794b2-119">**View 物件**</span><span class="sxs-lookup"><span data-stu-id="794b2-119">**View object**</span></span>](view-object.md)
-   <span data-ttu-id="794b2-120">[](record-stringdata.md) [ **Record 物件** 的至 convertfrom-stringdata 屬性](record-object.md)</span><span class="sxs-lookup"><span data-stu-id="794b2-120">[**StringData property**](record-stringdata.md) of the [**Record object**](record-object.md)</span></span>

<span data-ttu-id="794b2-121">您必須擁有 Windows Script Host 的 CScript.exe 或 WScript.exe 版本，才能使用此範例。</span><span class="sxs-lookup"><span data-stu-id="794b2-121">You must have the CScript.exe or WScript.exe version of Windows Script Host to use this sample.</span></span> <span data-ttu-id="794b2-122">若要使用 CScript.exe 執行此範例，請使用下列語法在命令提示字元中輸入命令列。</span><span class="sxs-lookup"><span data-stu-id="794b2-122">To use CScript.exe to run this sample, type a command line at the command prompt using the following syntax.</span></span> <span data-ttu-id="794b2-123">如果第一個引數是/？，則會顯示說明</span><span class="sxs-lookup"><span data-stu-id="794b2-123">Help is displayed if the first argument is /?</span></span> <span data-ttu-id="794b2-124">或者，如果指定的引數太少。</span><span class="sxs-lookup"><span data-stu-id="794b2-124">or if too few arguments are specified.</span></span> <span data-ttu-id="794b2-125">若要將輸出重新導向至檔案，請以 VBS > 路徑結束命令列 \[ \] 。</span><span class="sxs-lookup"><span data-stu-id="794b2-125">To redirect the output to a file, end the command line with VBS > \[path to file\].</span></span> <span data-ttu-id="794b2-126">此範例會傳回值0表示成功，如果叫用說明，則傳回 1; 如果腳本失敗，則傳回2。</span><span class="sxs-lookup"><span data-stu-id="794b2-126">The sample returns a value of 0 for success, 1 if help is invoked, and 2 if the script fails.</span></span>

<span data-ttu-id="794b2-127">**cscript WiMerge.vbs \[ 路徑指向匯 \] \[ 入資料庫 \] \[ 資料表名稱的資料庫路徑\]**</span><span class="sxs-lookup"><span data-stu-id="794b2-127">**cscript WiMerge.vbs \[path to database\]\[path to imported database\]\[table name\]**</span></span>

<span data-ttu-id="794b2-128">指定接收合併之 Windows Installer 資料庫的路徑。</span><span class="sxs-lookup"><span data-stu-id="794b2-128">Specify the path to the Windows Installer database that is receiving the merge.</span></span> <span data-ttu-id="794b2-129">指定要匯入至第一個資料庫的路徑。</span><span class="sxs-lookup"><span data-stu-id="794b2-129">Specify the path to the database being imported into the first.</span></span> <span data-ttu-id="794b2-130">您可以為資料表指定選擇性的名稱來保存合併錯誤。</span><span class="sxs-lookup"><span data-stu-id="794b2-130">You may specify an optional name for a table to hold the merge errors.</span></span> <span data-ttu-id="794b2-131">如果未指定資料表名稱，安裝程式會使用名稱 \_ MergeErrors，並在顯示內容之後卸載資料表。</span><span class="sxs-lookup"><span data-stu-id="794b2-131">If no table name is specified, the installer uses the name \_MergeErrors and drops the table after displaying the contents.</span></span>

<span data-ttu-id="794b2-132">如需其他腳本範例，請參閱 [Windows Installer 腳本範例](windows-installer-scripting-examples.md)。</span><span class="sxs-lookup"><span data-stu-id="794b2-132">For additional scripting examples, see [Windows Installer Scripting Examples](windows-installer-scripting-examples.md).</span></span> <span data-ttu-id="794b2-133">如需不需要 Windows Script Host 的範例公用程式，請參閱 [Windows Installer 開發工具](windows-installer-development-tools.md)。</span><span class="sxs-lookup"><span data-stu-id="794b2-133">For sample utilities that do not require Windows Script Host, see [Windows Installer Development Tools](windows-installer-development-tools.md).</span></span>

 

 



