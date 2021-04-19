---
description: Windows Installer 開發人員 Windows SDK 元件中提供 VBScript 程式碼範例檔案 WiTextIn.vbs。
ms.assetid: ba6c6367-ebb1-4981-ae3a-bcff68aacdbf
title: 將 ANSI 檔案複製到資料庫欄位
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73dc6c4d3a945177581a35bf6b19d89855abb5ef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106974498"
---
# <a name="copy-ansi-file-into-a-database-field"></a><span data-ttu-id="f6d33-103">將 ANSI 檔案複製到資料庫欄位</span><span class="sxs-lookup"><span data-stu-id="f6d33-103">Copy ANSI File Into a Database Field</span></span>

<span data-ttu-id="f6d33-104">[Windows Installer 開發人員 Windows SDK 元件](platform-sdk-components-for-windows-installer-developers.md)中提供 VBScript 程式碼範例檔案 WiTextIn.vbs。</span><span class="sxs-lookup"><span data-stu-id="f6d33-104">The VBScript code sample file WiTextIn.vbs is provided in the [Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).</span></span> <span data-ttu-id="f6d33-105">此範例會示範如何使用腳本，將檔案複製到 Windows Installer 資料庫的文字欄位中，並示範主鍵資料的處理方式。</span><span class="sxs-lookup"><span data-stu-id="f6d33-105">The sample shows how a script can be used to copy a file into a text field of a Windows Installer database, and demonstrates the processing of primary key data.</span></span>

<span data-ttu-id="f6d33-106">程式碼範例也會顯示下列各項：</span><span class="sxs-lookup"><span data-stu-id="f6d33-106">The code sample also shows you the following:</span></span>

-   <span data-ttu-id="f6d33-107">[**OpenDatabase 方法 (安裝程式物件)**](installer-opendatabase.md)和 [**安裝程式物件**](installer-object.md)的 [**LastErrorRecord 方法**](installer-lasterrorrecord.md)</span><span class="sxs-lookup"><span data-stu-id="f6d33-107">[**OpenDatabase method (Installer Object)**](installer-opendatabase.md) and the [**LastErrorRecord method**](installer-lasterrorrecord.md) of the [**Installer Object**](installer-object.md)</span></span>
-   <span data-ttu-id="f6d33-108">[**OpenView 方法**](database-openview.md)、 [**Commit 方法**](database-commit.md)和 [**Database 物件**](database-object.md)的 [**PrimaryKeys 屬性**](database-primarykeys.md)</span><span class="sxs-lookup"><span data-stu-id="f6d33-108">[**OpenView method**](database-openview.md), the [**Commit method**](database-commit.md), and the [**PrimaryKeys property**](database-primarykeys.md) of the [**Database Object**](database-object.md)</span></span>
-   <span data-ttu-id="f6d33-109">[**View 物件**](view-object.md)的 [**Fetch 方法**](view-fetch.md)和 [**Modify 方法**](view-modify.md)</span><span class="sxs-lookup"><span data-stu-id="f6d33-109">[**Fetch method**](view-fetch.md) and the [**Modify method**](view-modify.md) of the [**View Object**](view-object.md)</span></span>
-   <span data-ttu-id="f6d33-110">[**Record 物件**](record-object.md)的 [**至 convertfrom-stringdata 屬性**](record-stringdata.md)和 [**ReadStream 方法**](record-readstream.md)</span><span class="sxs-lookup"><span data-stu-id="f6d33-110">[**StringData property**](record-stringdata.md) and [**ReadStream method**](record-readstream.md) of the [**Record Object**](record-object.md)</span></span>

<span data-ttu-id="f6d33-111">若要使用程式碼範例，您需要 Windows Script Host 的 CScript.exe 或 WScript.exe 版本。</span><span class="sxs-lookup"><span data-stu-id="f6d33-111">To use the code sample you need the CScript.exe or WScript.exe version of Windows Script Host.</span></span>

<span data-ttu-id="f6d33-112">**使用 CScript.exe 來執行此範例**</span><span class="sxs-lookup"><span data-stu-id="f6d33-112">**To use CScript.exe to run this sample**</span></span>

-   <span data-ttu-id="f6d33-113">在命令提示字元中，輸入下列語法：</span><span class="sxs-lookup"><span data-stu-id="f6d33-113">At the command prompt, type the following syntax:</span></span>

    <span data-ttu-id="f6d33-114">**cscript WiTextIn.vbs \[ 路徑指向資料庫 \] \[ 資料表名稱 \] \[ 主鍵值的資料 \] \[ 行名稱 \] \[ 路徑\]**</span><span class="sxs-lookup"><span data-stu-id="f6d33-114">**cscript WiTextIn.vbs \[path to database\]\[table name\]\[primary key values\]\[column name\]\[path to file\]**</span></span>

> [!Note]  
> <span data-ttu-id="f6d33-115">如果第一個引數是/？，則會顯示說明</span><span class="sxs-lookup"><span data-stu-id="f6d33-115">Help is displayed if the first argument is /?</span></span> <span data-ttu-id="f6d33-116">或者，如果指定的引數太少。</span><span class="sxs-lookup"><span data-stu-id="f6d33-116">or if too few arguments are specified.</span></span>

 

<span data-ttu-id="f6d33-117">**將輸出重新導向至檔案**</span><span class="sxs-lookup"><span data-stu-id="f6d33-117">**To redirect the output to a file**</span></span>

-   <span data-ttu-id="f6d33-118">以下列： **VBS > 檔案路徑結束命令列 \[ \] 。T**</span><span class="sxs-lookup"><span data-stu-id="f6d33-118">End the command line with the following: **VBS > \[path to file\]. T**</span></span>

> [!Note]  
> <span data-ttu-id="f6d33-119">此範例會傳回值 0 (零) 表示成功，1 (一個) （如果叫用說明），而如果腳本失敗，則為 2 (兩個) 。</span><span class="sxs-lookup"><span data-stu-id="f6d33-119">The sample returns a value of 0 (zero) for success, 1 (one) if Help is invoked, and 2 (two) if the script fails.</span></span>

 

<span data-ttu-id="f6d33-120">下列清單會識別您必須指定的專案：</span><span class="sxs-lookup"><span data-stu-id="f6d33-120">The following list identifies the items that you must specify:</span></span>

-   <span data-ttu-id="f6d33-121">指定 Windows Installer 資料庫的路徑。</span><span class="sxs-lookup"><span data-stu-id="f6d33-121">Specify the path to the Windows Installer database.</span></span>
-   <span data-ttu-id="f6d33-122">指定資料庫資料表的名稱。</span><span class="sxs-lookup"><span data-stu-id="f6d33-122">Specify the name of the database table.</span></span>
-   <span data-ttu-id="f6d33-123">依序指定資料列的所有主要索引鍵值，並以冒號串連。</span><span class="sxs-lookup"><span data-stu-id="f6d33-123">Specify all the primary key values for the row, in order, and concatenated with colons.</span></span>
-   <span data-ttu-id="f6d33-124">請指定不是索引鍵資料行的資料行名稱。</span><span class="sxs-lookup"><span data-stu-id="f6d33-124">Specify a column name that is not a key column.</span></span> <span data-ttu-id="f6d33-125">這是您想要接收資料的資料行。</span><span class="sxs-lookup"><span data-stu-id="f6d33-125">This is the column that you want to receive the data.</span></span>
-   <span data-ttu-id="f6d33-126">指定要複製之文字檔的路徑。</span><span class="sxs-lookup"><span data-stu-id="f6d33-126">Specify the path to the text file that is being copied.</span></span>

> [!Note]  
> <span data-ttu-id="f6d33-127">如果省略最後一個引數，則會顯示欄位中目前的值。</span><span class="sxs-lookup"><span data-stu-id="f6d33-127">If the last argument is omitted, the current value in the field is displayed.</span></span>

 

<span data-ttu-id="f6d33-128">如需其他腳本範例，請參閱 [Windows Installer 腳本範例](windows-installer-scripting-examples.md)。</span><span class="sxs-lookup"><span data-stu-id="f6d33-128">For more scripting examples, see [Windows Installer Scripting Examples](windows-installer-scripting-examples.md).</span></span> <span data-ttu-id="f6d33-129">如需不需要 Windows Script Host 的範例公用程式，請參閱 [Windows Installer 開發工具](windows-installer-development-tools.md)。</span><span class="sxs-lookup"><span data-stu-id="f6d33-129">For sample utilities that do not require the Windows Script Host, see [Windows Installer Development Tools](windows-installer-development-tools.md).</span></span>

 

 



