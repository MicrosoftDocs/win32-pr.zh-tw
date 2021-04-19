---
description: Windows Installer 開發人員 Windows SDK 元件中提供了 VBScript 檔案 WiImport.vbs。 此範例示範如何撰寫腳本，以將資料表匯入 Windows Installer 資料庫。
ms.assetid: 37580bd6-30c7-4239-9717-223a381ba021
title: 匯入檔案
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8508ee4e385e3edc737515f1b524de074489fb2b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106998261"
---
# <a name="import-files"></a><span data-ttu-id="f636a-104">匯入檔案</span><span class="sxs-lookup"><span data-stu-id="f636a-104">Import Files</span></span>

<span data-ttu-id="f636a-105">[Windows Installer 開發人員 Windows SDK 元件](platform-sdk-components-for-windows-installer-developers.md)中提供了 VBScript 檔案 WiImport.vbs。</span><span class="sxs-lookup"><span data-stu-id="f636a-105">The VBScript file WiImport.vbs is provided in the [Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).</span></span> <span data-ttu-id="f636a-106">此範例示範如何撰寫腳本，以將資料表匯入 Windows Installer 資料庫。</span><span class="sxs-lookup"><span data-stu-id="f636a-106">This sample shows how to write a script to import tables into a Windows Installer database.</span></span>

<span data-ttu-id="f636a-107">腳本會連接到 [**安裝程式**](installer-object.md) 物件、開啟資料庫、處理檔案清單，並在關閉資料庫之前認可變更。</span><span class="sxs-lookup"><span data-stu-id="f636a-107">The script connects to an [**Installer**](installer-object.md) object, opens a database, processes a list of files, and commits the changes before closing the database.</span></span>

<span data-ttu-id="f636a-108">此範例將示範如何使用：</span><span class="sxs-lookup"><span data-stu-id="f636a-108">The sample demonstrates the use of:</span></span>

-   [<span data-ttu-id="f636a-109">**(安裝程式物件) 的 OpenDatabase 方法**</span><span class="sxs-lookup"><span data-stu-id="f636a-109">**OpenDatabase Method (Installer Object)**</span></span>](installer-opendatabase.md)
-   <span data-ttu-id="f636a-110">[](installer-lasterrorrecord.md) [**安裝程式物件** 的 LastErrorRecord 方法](installer-object.md)</span><span class="sxs-lookup"><span data-stu-id="f636a-110">[**LastErrorRecord method**](installer-lasterrorrecord.md) of the [**Installer object**](installer-object.md)</span></span>
-   [<span data-ttu-id="f636a-111">**Import 方法**</span><span class="sxs-lookup"><span data-stu-id="f636a-111">**Import method**</span></span>](database-import.md)
-   <span data-ttu-id="f636a-112">[](database-commit.md) [ **Database 物件** 的 Commit 方法](database-object.md)</span><span class="sxs-lookup"><span data-stu-id="f636a-112">[**Commit method**](database-commit.md) of the [**Database object**](database-object.md)</span></span>

<span data-ttu-id="f636a-113">您將需要 CScript.exe 或 WScript.exe 版本的 Windows Script Host 才能使用此範例。</span><span class="sxs-lookup"><span data-stu-id="f636a-113">You'll require the CScript.exe or WScript.exe version of Windows Script Host to use this sample.</span></span> <span data-ttu-id="f636a-114">若要使用 CScript.exe 執行此範例，請在命令提示字元中使用下列語法。</span><span class="sxs-lookup"><span data-stu-id="f636a-114">To use CScript.exe to run this sample, use the following syntax at the command prompt.</span></span>

<span data-ttu-id="f636a-115">**cscript WiImport.vbs \[ 路徑指向 \] \[ 資料夾 \] \[ 選項 \] \[ 保存檔案清單的資料庫路徑**\]</span><span class="sxs-lookup"><span data-stu-id="f636a-115">**cscript WiImport.vbs \[path to database\]\[path to folder\]\[options\] \[archive file list**\]</span></span>

<span data-ttu-id="f636a-116">如果第一個引數是/？，則會顯示說明</span><span class="sxs-lookup"><span data-stu-id="f636a-116">Help is displayed if the first argument is /?</span></span> <span data-ttu-id="f636a-117">或者，如果指定的引數太少。</span><span class="sxs-lookup"><span data-stu-id="f636a-117">or if too few arguments are specified.</span></span> <span data-ttu-id="f636a-118">若要將輸出重新導向至檔案，請以 VBS > 路徑結束命令列 \[ \] 。此範例會傳回值0表示成功，如果叫用說明，則傳回 1; 如果腳本失敗，則傳回2。</span><span class="sxs-lookup"><span data-stu-id="f636a-118">To redirect the output to a file, end the command line with VBS > \[path to file\].The sample returns a value of 0 for success, 1 if help is invoked, and 2 if the script fails.</span></span>

<span data-ttu-id="f636a-119">指定要建立或接收匯入之資料表的 Windows installer 資料庫路徑。</span><span class="sxs-lookup"><span data-stu-id="f636a-119">Specify the path to a Windows installer database that is to be created or that is to receive the imported tables.</span></span> <span data-ttu-id="f636a-120">指定包含要匯入之資料表保存檔案的資料夾路徑。</span><span class="sxs-lookup"><span data-stu-id="f636a-120">Specify the path to the folder containing the archive files of the tables that are being imported.</span></span> <span data-ttu-id="f636a-121">列出正在匯入的封存檔案名稱。</span><span class="sxs-lookup"><span data-stu-id="f636a-121">List the names of the archive files that are being imported.</span></span> <span data-ttu-id="f636a-122">萬用字元檔案名（例如 \* idt）可以用來匯入多個檔案。</span><span class="sxs-lookup"><span data-stu-id="f636a-122">Wildcard file names, such as \*.idt, can be used to import multiple files.</span></span>

<span data-ttu-id="f636a-123">您可以在檔案清單前的命令列上的任何位置指定下列選項。</span><span class="sxs-lookup"><span data-stu-id="f636a-123">The following options may be specified anywhere on the command line before the file list.</span></span>



| <span data-ttu-id="f636a-124">選項</span><span class="sxs-lookup"><span data-stu-id="f636a-124">Option</span></span>              | <span data-ttu-id="f636a-125">Description</span><span class="sxs-lookup"><span data-stu-id="f636a-125">Description</span></span>                                                                                                                          |
|---------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f636a-126">未指定任何選項</span><span class="sxs-lookup"><span data-stu-id="f636a-126">no option specified</span></span> | <span data-ttu-id="f636a-127">從指定的資料夾將資料表封存檔案清單匯入 Windows Installer 資料庫。</span><span class="sxs-lookup"><span data-stu-id="f636a-127">Import the list of table archive files from the specified folder into the Windows Installer database.</span></span>                                |
| <span data-ttu-id="f636a-128">/c</span><span class="sxs-lookup"><span data-stu-id="f636a-128">/c</span></span>                  | <span data-ttu-id="f636a-129">建立 Windows Installer 資料庫，然後從指定的資料夾將資料表封存檔案清單匯入至新的資料庫。</span><span class="sxs-lookup"><span data-stu-id="f636a-129">Create a Windows Installer database and then import the list of table archive files from the specified folder into the new database.</span></span> |



 

<span data-ttu-id="f636a-130">如需詳細資訊，請參閱 [Windows Installer 腳本範例](windows-installer-scripting-examples.md) ，以取得其他腳本範例。</span><span class="sxs-lookup"><span data-stu-id="f636a-130">For more information, see [Windows Installer Scripting Examples](windows-installer-scripting-examples.md) for additional scripting examples.</span></span> <span data-ttu-id="f636a-131">如需不需要 Windows Script Host 的範例公用程式，請參閱 [Windows Installer 開發工具](windows-installer-development-tools.md)。</span><span class="sxs-lookup"><span data-stu-id="f636a-131">For sample utilities that do not require Windows Script Host, see [Windows Installer Development Tools](windows-installer-development-tools.md).</span></span>

<span data-ttu-id="f636a-132">請注意， [當地語系化範例](a-localization-example.md) 也會示範如何匯 [入當地語系化的錯誤和 ActionText 資料表](importing-localized-error-and-actiontext-tables.md)。</span><span class="sxs-lookup"><span data-stu-id="f636a-132">Note that [A Localization Example](a-localization-example.md) also demonstrates [Importing Localized Error and ActionText Tables](importing-localized-error-and-actiontext-tables.md).</span></span>

 

 



