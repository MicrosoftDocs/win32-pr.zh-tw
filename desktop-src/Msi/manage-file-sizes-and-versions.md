---
description: Windows Installer 開發人員 Windows SDK 元件中提供了 VBScript 檔案 WiFilVer.vbs。 此範例會示範如何使用腳本來報告或更新檔案版本、大小和語言資訊。
ms.assetid: 21550eea-c30b-4738-9201-ab500356fabf
title: 管理檔案大小和版本
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 426acf71956d87fe1458447119d79bc142f1ee75
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103691064"
---
# <a name="manage-file-sizes-and-versions"></a><span data-ttu-id="749af-104">管理檔案大小和版本</span><span class="sxs-lookup"><span data-stu-id="749af-104">Manage File Sizes and Versions</span></span>

<span data-ttu-id="749af-105">[Windows Installer 開發人員 Windows SDK 元件](platform-sdk-components-for-windows-installer-developers.md)中提供了 VBScript 檔案 WiFilVer.vbs。</span><span class="sxs-lookup"><span data-stu-id="749af-105">The VBScript file WiFilVer.vbs is provided in the [Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).</span></span> <span data-ttu-id="749af-106">此範例會示範如何使用腳本來報告或更新檔案版本、大小和語言資訊。</span><span class="sxs-lookup"><span data-stu-id="749af-106">The sample shows you how you can use a script to report or update the file version, size, and language information.</span></span>

<span data-ttu-id="749af-107">此範例也會顯示 Windows Installer 動作、如何存取 Windows Installer 資料庫，以及如何使用下列各項：</span><span class="sxs-lookup"><span data-stu-id="749af-107">The sample also shows you Windows Installer actions, how to access a Windows Installer database, and the use of the following:</span></span>

-   <span data-ttu-id="749af-108">[](installer-opendatabase.md) [**安裝程式物件** 的 OpenDatabase 方法](installer-object.md)</span><span class="sxs-lookup"><span data-stu-id="749af-108">[**Installer.OpenDatabase**](installer-opendatabase.md) method of the [**Installer Object**](installer-object.md)</span></span>
-   <span data-ttu-id="749af-109">[**FileAttributes**](installer-fileattributes.md) 屬性</span><span class="sxs-lookup"><span data-stu-id="749af-109">[**Installer.FileAttributes**](installer-fileattributes.md) property</span></span>
-   <span data-ttu-id="749af-110">[**Get-filehash**](installer-filehash.md) 方法</span><span class="sxs-lookup"><span data-stu-id="749af-110">[**Installer.FileHash**](installer-filehash.md) method</span></span>
-   <span data-ttu-id="749af-111">[**FileVersion**](installer-fileversion.md) 方法</span><span class="sxs-lookup"><span data-stu-id="749af-111">[**Installer.FileVersion**](installer-fileversion.md) method</span></span>
-   <span data-ttu-id="749af-112">[](installer-lasterrorrecord.md) [**安裝程式物件** 的 LastErrorRecord 方法](installer-object.md)</span><span class="sxs-lookup"><span data-stu-id="749af-112">[**Installer.LastErrorRecord**](installer-lasterrorrecord.md) method of the [**Installer Object**](installer-object.md)</span></span>
-   <span data-ttu-id="749af-113">[**資料庫. OpenView**](database-openview.md) 方法</span><span class="sxs-lookup"><span data-stu-id="749af-113">[**Database.OpenView**](database-openview.md) method</span></span>
-   <span data-ttu-id="749af-114">[](database-summaryinformation.md) [ **Database 物件** 的 SummaryInformation 屬性](database-object.md)</span><span class="sxs-lookup"><span data-stu-id="749af-114">[**Database.SummaryInformation**](database-summaryinformation.md) property of the [**Database Object**](database-object.md)</span></span>
-   <span data-ttu-id="749af-115">[**Dataadapter.doaction**](session-doaction.md) 方法</span><span class="sxs-lookup"><span data-stu-id="749af-115">[**Session.DoAction**](session-doaction.md) method</span></span>
-   [<span data-ttu-id="749af-116">**Session. 屬性**</span><span class="sxs-lookup"><span data-stu-id="749af-116">**Session.Property**</span></span>](session-session.md)
-   <span data-ttu-id="749af-117">[**Session**](session-sourcepath.md) 屬性</span><span class="sxs-lookup"><span data-stu-id="749af-117">[**Session.SourcePath**](session-sourcepath.md) property</span></span>
-   <span data-ttu-id="749af-118">Session 物件的 [**session. Mode**](session-mode.md)屬性 [](session-object.md)</span><span class="sxs-lookup"><span data-stu-id="749af-118">[**Session.Mode**](session-mode.md) property of the [**Session Object**](session-object.md)</span></span>
-   <span data-ttu-id="749af-119">[**至 convertfrom-stringdata**](record-stringdata.md) 屬性</span><span class="sxs-lookup"><span data-stu-id="749af-119">[**Record.StringData**](record-stringdata.md) property</span></span>
-   <span data-ttu-id="749af-120">[](record-integerdata.md) [ **Record 物件** 的 IntegerData 屬性](record-object.md)</span><span class="sxs-lookup"><span data-stu-id="749af-120">[**Record.IntegerData**](record-integerdata.md) property of the [**Record Object**](record-object.md)</span></span>

<span data-ttu-id="749af-121">使用此範例需要 Windows Script Host 的 CScript.exe 或 WScript.exe 版本。</span><span class="sxs-lookup"><span data-stu-id="749af-121">Using this sample requires the CScript.exe or WScript.exe version of Windows Script Host.</span></span> <span data-ttu-id="749af-122">若要使用 CScript.exe 執行此範例，請使用下列語法在命令提示字元中輸入命令：</span><span class="sxs-lookup"><span data-stu-id="749af-122">To use CScript.exe to run this sample, type a command at the command prompt by using the following syntax:</span></span>

<span data-ttu-id="749af-123">**cscript WiFilVer.vbs \[ 資料庫 \] \[ 選擇性來源位置的路徑\]**</span><span class="sxs-lookup"><span data-stu-id="749af-123">**cscript WiFilVer.vbs \[path to database\]\[optional source locations\]**</span></span>

<span data-ttu-id="749af-124">也請注意下列事項：</span><span class="sxs-lookup"><span data-stu-id="749af-124">Also be aware of the following:</span></span>

-   <span data-ttu-id="749af-125">如果第一個引數是/？，則會顯示說明</span><span class="sxs-lookup"><span data-stu-id="749af-125">Help is displayed if the first argument is /?</span></span> <span data-ttu-id="749af-126">或者，如果指定的引數太少。</span><span class="sxs-lookup"><span data-stu-id="749af-126">or if too few arguments are specified.</span></span>
-   <span data-ttu-id="749af-127">若要將輸出重新導向至檔案，請以 VBS > 路徑結束命令列 \[  \] 。</span><span class="sxs-lookup"><span data-stu-id="749af-127">To redirect the output to a file, end the command line with VBS > \[*path to file*\].</span></span>
-   <span data-ttu-id="749af-128">此範例會傳回值 0 (零) 表示成功，1 (一個) （如果叫用說明），而如果腳本失敗，則為 2 (兩個) 。</span><span class="sxs-lookup"><span data-stu-id="749af-128">The sample returns a value of 0 (zero) for success, 1 (one) if help is invoked, and 2 (two) if the script fails.</span></span>

<span data-ttu-id="749af-129">指定您要更新的 Windows Installer 資料庫（必須位於原始程式檔根目錄）。</span><span class="sxs-lookup"><span data-stu-id="749af-129">Specify the Windows Installer database that you want to be updated, which must be located at the source file root.</span></span> <span data-ttu-id="749af-130">不過，您可以在不同的位置指定資料庫的來源。</span><span class="sxs-lookup"><span data-stu-id="749af-130">However, you can specify sources for the database at separate locations.</span></span> <span data-ttu-id="749af-131">如果來源是壓縮的，則會在根目錄開啟所有檔案。</span><span class="sxs-lookup"><span data-stu-id="749af-131">If the source is compressed, all the files are opened at the root.</span></span>

<span data-ttu-id="749af-132">您可以在命令列上的任何位置指定下列選項。</span><span class="sxs-lookup"><span data-stu-id="749af-132">The following options can be specified at any location on the command line.</span></span>



| <span data-ttu-id="749af-133">選項</span><span class="sxs-lookup"><span data-stu-id="749af-133">Option</span></span>                | <span data-ttu-id="749af-134">Description</span><span class="sxs-lookup"><span data-stu-id="749af-134">Description</span></span>                                                                              |
|-----------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="749af-135">*未指定任何選項*</span><span class="sxs-lookup"><span data-stu-id="749af-135">*no option specified*</span></span> | <span data-ttu-id="749af-136">顯示資料庫的檔案資訊。</span><span class="sxs-lookup"><span data-stu-id="749af-136">Display the file information of the database.</span></span>                                            |
| <span data-ttu-id="749af-137">/U</span><span class="sxs-lookup"><span data-stu-id="749af-137">/u</span></span>                    | <span data-ttu-id="749af-138">從來源更新資料庫中的檔案大小、版本和語言資訊。</span><span class="sxs-lookup"><span data-stu-id="749af-138">Update the file size, version, and language information in the database from the source.</span></span> |



 

<span data-ttu-id="749af-139">如需詳細資訊，請參閱 [Windows Installer 腳本範例](windows-installer-scripting-examples.md) 和 [Windows Installer 開發工具](windows-installer-development-tools.md)。</span><span class="sxs-lookup"><span data-stu-id="749af-139">For more information, see [Windows Installer Scripting Examples](windows-installer-scripting-examples.md) and [Windows Installer Development Tools](windows-installer-development-tools.md).</span></span>

 

 



