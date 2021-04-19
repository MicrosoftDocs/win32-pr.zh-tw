---
description: Windows Installer 開發人員 Windows SDK 元件中提供了 VBScript 檔案 WiExport.vbs。
ms.assetid: 3ff7bd48-cb22-4d5b-a607-39eaeb67c55b
title: 匯出檔案
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1512650ee144fc00c2de851051b9bbb4d98a21e0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106979051"
---
# <a name="export-files"></a><span data-ttu-id="97d2b-103">匯出檔案</span><span class="sxs-lookup"><span data-stu-id="97d2b-103">Export Files</span></span>

<span data-ttu-id="97d2b-104">[Windows Installer 開發人員 Windows SDK 元件](platform-sdk-components-for-windows-installer-developers.md)中提供了 VBScript 檔案 WiExport.vbs。</span><span class="sxs-lookup"><span data-stu-id="97d2b-104">The VBScript file WiExport.vbs is provided in the [Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).</span></span> <span data-ttu-id="97d2b-105">此範例示範如何撰寫腳本，以將資料表匯出至 Windows Installer 資料庫。</span><span class="sxs-lookup"><span data-stu-id="97d2b-105">This sample shows how to write script to export tables into a Windows Installer database.</span></span> <span data-ttu-id="97d2b-106">腳本範例會連接到 [**安裝程式**](installer-object.md) 物件、開啟資料庫，並將資料表匯出到封存檔案。</span><span class="sxs-lookup"><span data-stu-id="97d2b-106">The script sample connects to an [**Installer**](installer-object.md) object, opens a database and exports tables to archive files.</span></span>

<span data-ttu-id="97d2b-107">此範例將示範如何使用：</span><span class="sxs-lookup"><span data-stu-id="97d2b-107">The sample demonstrates the use of:</span></span>

-   [<span data-ttu-id="97d2b-108">**(安裝程式物件) 的 OpenDatabase 方法**</span><span class="sxs-lookup"><span data-stu-id="97d2b-108">**OpenDatabase Method (Installer Object)**</span></span>](installer-opendatabase.md)
-   <span data-ttu-id="97d2b-109">[](installer-lasterrorrecord.md) [**安裝程式物件** 的 LastErrorRecord 方法](installer-object.md)</span><span class="sxs-lookup"><span data-stu-id="97d2b-109">[**LastErrorRecord method**](installer-lasterrorrecord.md) of the [**Installer object**](installer-object.md)</span></span>
-   [<span data-ttu-id="97d2b-110">**Export 方法**</span><span class="sxs-lookup"><span data-stu-id="97d2b-110">**Export method**</span></span>](database-export.md)
-   <span data-ttu-id="97d2b-111">[](database-openview.md) [**資料庫物件** 的 OpenView 方法](database-object.md)</span><span class="sxs-lookup"><span data-stu-id="97d2b-111">[**OpenView method**](database-openview.md) of the [**Database object**](database-object.md)</span></span>
-   <span data-ttu-id="97d2b-112">[](view-fetch.md) [ **View 物件** 的 Fetch 方法](view-object.md)</span><span class="sxs-lookup"><span data-stu-id="97d2b-112">[**Fetch method**](view-fetch.md) of the [**View object**](view-object.md)</span></span>
-   <span data-ttu-id="97d2b-113">[](record-stringdata.md) [ **Record 物件** 的至 convertfrom-stringdata 屬性](record-object.md)</span><span class="sxs-lookup"><span data-stu-id="97d2b-113">[**StringData property**](record-stringdata.md) of the [**Record object**](record-object.md)</span></span>

<span data-ttu-id="97d2b-114">您將需要 CScript.exe 或 WScript.exe 版本的 Windows Script Host 才能使用此範例。</span><span class="sxs-lookup"><span data-stu-id="97d2b-114">You'll require the CScript.exe or WScript.exe version of Windows Script Host to use this sample.</span></span> <span data-ttu-id="97d2b-115">若要使用 CScript.exe 執行此範例，請使用下列語法在命令提示字元中輸入命令列。</span><span class="sxs-lookup"><span data-stu-id="97d2b-115">To use CScript.exe to run this sample, type a command line at the command prompt using the following syntax.</span></span> <span data-ttu-id="97d2b-116">如果第一個引數是/？，則會顯示說明</span><span class="sxs-lookup"><span data-stu-id="97d2b-116">Help is displayed if the first argument is /?</span></span> <span data-ttu-id="97d2b-117">或者，如果指定的引數太少。</span><span class="sxs-lookup"><span data-stu-id="97d2b-117">or if too few arguments are specified.</span></span> <span data-ttu-id="97d2b-118">若要將輸出重新導向至檔案，請以 VBS > 路徑結束命令列 \[  \] 。</span><span class="sxs-lookup"><span data-stu-id="97d2b-118">To redirect the output to a file, end the command line with VBS > \[*path to file*\].</span></span> <span data-ttu-id="97d2b-119">此範例會傳回值0表示成功，如果叫用說明，則傳回 1; 如果腳本失敗，則傳回2。</span><span class="sxs-lookup"><span data-stu-id="97d2b-119">The sample returns a value of 0 for success, 1 if help is invoked, and 2 if the script fails.</span></span>

<span data-ttu-id="97d2b-120">**cscript WiExport.vbs \[ 路徑指向 \] \[ 資料夾 \] \[ 選項 \] \[ 資料表名稱清單的資料庫路徑\]**</span><span class="sxs-lookup"><span data-stu-id="97d2b-120">**cscript WiExport.vbs \[path to database\]\[path to folder\]\[options\]\[table name list\]**</span></span>

<span data-ttu-id="97d2b-121">指定要從中匯出資料表的安裝程式資料庫路徑。</span><span class="sxs-lookup"><span data-stu-id="97d2b-121">Specify the path to the installer database from which the tables are being exported.</span></span> <span data-ttu-id="97d2b-122">指定要將匯出的封存檔案複製到其中的資料夾路徑。</span><span class="sxs-lookup"><span data-stu-id="97d2b-122">Specify the path to the folder into which the exported archive files are to be copied.</span></span> <span data-ttu-id="97d2b-123">列出要匯出的 [資料庫資料表](database-tables.md) 名稱（區分大小寫）。</span><span class="sxs-lookup"><span data-stu-id="97d2b-123">List the case-sensitive names of the [database tables](database-tables.md) being exported.</span></span> <span data-ttu-id="97d2b-124">指定 ' \* ' 以匯出所有資料表（包括 \_ SummaryInformation）。</span><span class="sxs-lookup"><span data-stu-id="97d2b-124">Specify '\*' to export all the tables including \_SummaryInformation.</span></span>

<span data-ttu-id="97d2b-125">您可以在命令列上的任何位置指定下列選項，在資料表名稱清單之前。</span><span class="sxs-lookup"><span data-stu-id="97d2b-125">The following options may be specified anywhere on the command line before the table name list.</span></span>



| <span data-ttu-id="97d2b-126">選項</span><span class="sxs-lookup"><span data-stu-id="97d2b-126">Option</span></span>              | <span data-ttu-id="97d2b-127">Description</span><span class="sxs-lookup"><span data-stu-id="97d2b-127">Description</span></span>                                            |
|---------------------|--------------------------------------------------------|
| <span data-ttu-id="97d2b-128">未指定任何選項</span><span class="sxs-lookup"><span data-stu-id="97d2b-128">no option specified</span></span> | <span data-ttu-id="97d2b-129">匯出的封存檔案的檔案名可能很長。</span><span class="sxs-lookup"><span data-stu-id="97d2b-129">Exported archive files may have a long file name.</span></span>      |
| <span data-ttu-id="97d2b-130">/s</span><span class="sxs-lookup"><span data-stu-id="97d2b-130">/s</span></span>                  | <span data-ttu-id="97d2b-131">強制匯出的封存檔案具有簡短的檔案名。</span><span class="sxs-lookup"><span data-stu-id="97d2b-131">Force exported archive files to have short file names.</span></span> |



 

<span data-ttu-id="97d2b-132">如需其他腳本範例，請參閱 [Windows Installer 腳本範例](windows-installer-scripting-examples.md)。</span><span class="sxs-lookup"><span data-stu-id="97d2b-132">For additional scripting examples, see [Windows Installer Scripting Examples](windows-installer-scripting-examples.md).</span></span> <span data-ttu-id="97d2b-133">如需不需要 Windows Script Host 的範例公用程式，請參閱 [Windows Installer 開發工具](windows-installer-development-tools.md)。</span><span class="sxs-lookup"><span data-stu-id="97d2b-133">For sample utilities that do not require Windows Script Host, see [Windows Installer Development Tools](windows-installer-development-tools.md).</span></span>

 

 



