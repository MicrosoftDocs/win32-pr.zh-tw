---
description: Windows Installer 開發人員 Windows SDK 元件中提供了 VBScript 檔案 WiStream.vbs。
ms.assetid: f96d1fdd-81c8-4fb2-a23e-fda49ace8bef
title: 管理二進位資料流程
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 877631a40157a5d286ef0c2575732a6d561eefb8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106980459"
---
# <a name="manage-binary-streams"></a><span data-ttu-id="4fa97-103">管理二進位資料流程</span><span class="sxs-lookup"><span data-stu-id="4fa97-103">Manage Binary Streams</span></span>

<span data-ttu-id="4fa97-104">[Windows Installer 開發人員 Windows SDK 元件](platform-sdk-components-for-windows-installer-developers.md)中提供了 VBScript 檔案 WiStream.vbs。</span><span class="sxs-lookup"><span data-stu-id="4fa97-104">The VBScript file WiStream.vbs is provided in the [Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).</span></span> <span data-ttu-id="4fa97-105">這個範例會示範如何使用腳本來管理 Windows Installer 資料庫中的二進位資料流程。</span><span class="sxs-lookup"><span data-stu-id="4fa97-105">This sample shows how script can be used to manage binary streams in a Windows Installer database.</span></span> <span data-ttu-id="4fa97-106">範例可以用來將壓縮的檔案封包輸入至資料庫。</span><span class="sxs-lookup"><span data-stu-id="4fa97-106">The sample may be used to enter compressed file cabinets into a database.</span></span> <span data-ttu-id="4fa97-107">這個範例會示範 Windows Installer 資料庫中[ \_ 資料流程資料表](-streams-table.md)的作業。</span><span class="sxs-lookup"><span data-stu-id="4fa97-107">This sample demonstrates the operation of the [\_Streams table](-streams-table.md) in the Windows Installer database.</span></span>

<span data-ttu-id="4fa97-108">此範例也會示範如何使用：</span><span class="sxs-lookup"><span data-stu-id="4fa97-108">The sample also demonstrates the use of:</span></span>

-   [<span data-ttu-id="4fa97-109">**(安裝程式物件) 的 OpenDatabase 方法**</span><span class="sxs-lookup"><span data-stu-id="4fa97-109">**OpenDatabase method (Installer Object)**</span></span>](installer-opendatabase.md)
-   [<span data-ttu-id="4fa97-110">**CreateRecord 方法**</span><span class="sxs-lookup"><span data-stu-id="4fa97-110">**CreateRecord method**</span></span>](installer-createrecord.md)
-   <span data-ttu-id="4fa97-111">[](installer-lasterrorrecord.md) [**安裝程式物件** 的 LastErrorRecord 方法](installer-object.md)</span><span class="sxs-lookup"><span data-stu-id="4fa97-111">[**LastErrorRecord method**](installer-lasterrorrecord.md) of the [**Installer object**](installer-object.md)</span></span>
-   [<span data-ttu-id="4fa97-112">**OpenView 方法**</span><span class="sxs-lookup"><span data-stu-id="4fa97-112">**OpenView method**</span></span>](database-openview.md)
-   <span data-ttu-id="4fa97-113">[](database-commit.md) [ **Database 物件** 的 Commit 方法](database-object.md)</span><span class="sxs-lookup"><span data-stu-id="4fa97-113">[**Commit method**](database-commit.md) of the [**Database object**](database-object.md)</span></span>
-   [<span data-ttu-id="4fa97-114">**Fetch 方法**</span><span class="sxs-lookup"><span data-stu-id="4fa97-114">**Fetch method**</span></span>](view-fetch.md)
-   [<span data-ttu-id="4fa97-115">**Modify 方法**</span><span class="sxs-lookup"><span data-stu-id="4fa97-115">**Modify method**</span></span>](view-modify.md)
-   <span data-ttu-id="4fa97-116">[](view-execute.md) [ **View 物件** 的 Execute 方法](view-object.md)</span><span class="sxs-lookup"><span data-stu-id="4fa97-116">[**Execute method**](view-execute.md) of the [**View object**](view-object.md)</span></span>
-   [<span data-ttu-id="4fa97-117">**至 convertfrom-stringdata 屬性**</span><span class="sxs-lookup"><span data-stu-id="4fa97-117">**StringData property**</span></span>](record-stringdata.md)
-   <span data-ttu-id="4fa97-118">[](record-setstream.md) [ **Record 物件** 的 SetStream 方法](record-object.md)</span><span class="sxs-lookup"><span data-stu-id="4fa97-118">[**SetStream method**](record-setstream.md) of the [**Record object**](record-object.md)</span></span>

<span data-ttu-id="4fa97-119">您將需要 CScript.exe 或 WScript.exe 版本的 Windows Script Host 才能使用此範例。</span><span class="sxs-lookup"><span data-stu-id="4fa97-119">You'll require the CScript.exe or WScript.exe version of Windows Script Host to use this sample.</span></span> <span data-ttu-id="4fa97-120">若要使用 CScript.exe 執行此範例，請使用下列語法在命令提示字元中輸入命令列。</span><span class="sxs-lookup"><span data-stu-id="4fa97-120">To use CScript.exe to run this sample, type a command line at the command prompt using the following syntax.</span></span> <span data-ttu-id="4fa97-121">如果第一個引數是/？，則會顯示說明</span><span class="sxs-lookup"><span data-stu-id="4fa97-121">Help is displayed if the first argument is /?</span></span> <span data-ttu-id="4fa97-122">或者，如果指定的引數太少。</span><span class="sxs-lookup"><span data-stu-id="4fa97-122">or if too few arguments are specified.</span></span> <span data-ttu-id="4fa97-123">若要將輸出重新導向至檔案，請以 VBS > 路徑結束命令列 \[  \] 。</span><span class="sxs-lookup"><span data-stu-id="4fa97-123">To redirect the output to a file, end the command line with VBS > \[*path to file*\].</span></span> <span data-ttu-id="4fa97-124">此範例會傳回值0表示成功，如果叫用說明，則傳回 1; 如果腳本失敗，則傳回2。</span><span class="sxs-lookup"><span data-stu-id="4fa97-124">The sample returns a value of 0 for success, 1 if help is invoked, and 2 if the script fails.</span></span>

<span data-ttu-id="4fa97-125">**cscript WiStream.vbs \[ 路徑指向檔案 \] \[ \] \[ 選項 \] \[ 資料流程名稱的資料庫路徑\]**</span><span class="sxs-lookup"><span data-stu-id="4fa97-125">**cscript WiStream.vbs \[path to database\]\[path to file\]\[options\]\[stream name\]**</span></span>

<span data-ttu-id="4fa97-126">指定接收資料流程之 Windows Installer 資料庫的路徑。</span><span class="sxs-lookup"><span data-stu-id="4fa97-126">Specify the path to the Windows Installer database that is to receive the stream.</span></span> <span data-ttu-id="4fa97-127">指定包含資料流程資料之二進位檔案的路徑。</span><span class="sxs-lookup"><span data-stu-id="4fa97-127">Specify a path to the binary file containing the stream data.</span></span> <span data-ttu-id="4fa97-128">若要列出安裝程式資料庫中的資料流程，請省略此路徑。</span><span class="sxs-lookup"><span data-stu-id="4fa97-128">To list the streams in the installer database, omit this path.</span></span> <span data-ttu-id="4fa97-129">您可以指定選擇性的資料流程名稱，如果省略，則會預設為檔案名。</span><span class="sxs-lookup"><span data-stu-id="4fa97-129">You may specify an optional stream name, if this is omitted it defaults to the file name.</span></span>

<span data-ttu-id="4fa97-130">您可以指定下列選項。</span><span class="sxs-lookup"><span data-stu-id="4fa97-130">The following option may be specified.</span></span>



| <span data-ttu-id="4fa97-131">選項</span><span class="sxs-lookup"><span data-stu-id="4fa97-131">Option</span></span>              | <span data-ttu-id="4fa97-132">Description</span><span class="sxs-lookup"><span data-stu-id="4fa97-132">Description</span></span>                                                                                     |
|---------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4fa97-133">未指定任何選項</span><span class="sxs-lookup"><span data-stu-id="4fa97-133">no option specified</span></span> | <span data-ttu-id="4fa97-134">將資料流程新增至 Windows Installer 資料庫。</span><span class="sxs-lookup"><span data-stu-id="4fa97-134">Add a stream to the Windows Installer database.</span></span>                                                 |
| <span data-ttu-id="4fa97-135">/d</span><span class="sxs-lookup"><span data-stu-id="4fa97-135">/d</span></span>                  | <span data-ttu-id="4fa97-136">移除資料流程。</span><span class="sxs-lookup"><span data-stu-id="4fa97-136">Remove a stream.</span></span> <span data-ttu-id="4fa97-137">此選項旗標後面必須接著要移除之 substorage 的名稱。</span><span class="sxs-lookup"><span data-stu-id="4fa97-137">This option flag must be followed by the name of the substorage being removed.</span></span> |



 

<span data-ttu-id="4fa97-138">如需其他腳本範例，請參閱 [Windows Installer 腳本範例](windows-installer-scripting-examples.md)。</span><span class="sxs-lookup"><span data-stu-id="4fa97-138">For additional scripting examples, see [Windows Installer Scripting Examples](windows-installer-scripting-examples.md).</span></span> <span data-ttu-id="4fa97-139">如需不需要 Windows Script Host 的範例公用程式，請參閱 [Windows Installer 開發工具](windows-installer-development-tools.md)。</span><span class="sxs-lookup"><span data-stu-id="4fa97-139">For sample utilities that do not require Windows Script Host, see [Windows Installer Development Tools](windows-installer-development-tools.md).</span></span>

 

 



