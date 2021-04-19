---
description: Windows Installer 開發人員 Windows SDK 元件中提供了 VBScript 檔案 WiRunSQL.vbs。
ms.assetid: 1027b187-1237-43d1-9905-8fcdaec63903
title: 執行 SQL 語句
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99da54f85b02ee867003b140d505f5754f58cc00
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106996692"
---
# <a name="execute-sql-statements"></a><span data-ttu-id="65f35-103">執行 SQL 語句</span><span class="sxs-lookup"><span data-stu-id="65f35-103">Execute SQL Statements</span></span>

<span data-ttu-id="65f35-104">[Windows Installer 開發人員 Windows SDK 元件](platform-sdk-components-for-windows-installer-developers.md)中提供了 VBScript 檔案 WiRunSQL.vbs。</span><span class="sxs-lookup"><span data-stu-id="65f35-104">The VBScript file WiRunSQL.vbs is provided in the [Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).</span></span> <span data-ttu-id="65f35-105">此範例說明如何使用腳本來對 Windows Installer 資料庫執行 SQL 查詢和更新。</span><span class="sxs-lookup"><span data-stu-id="65f35-105">This sample shows how script is used to run SQL queries and updates against a Windows Installer database.</span></span> <span data-ttu-id="65f35-106">如需詳細資訊，請參閱 [Sql 語法](sql-syntax.md) 和 [使用 sql 和腳本的資料庫查詢範例](examples-of-database-queries-using-sql-and-script.md)。</span><span class="sxs-lookup"><span data-stu-id="65f35-106">For more information, see [SQL Syntax](sql-syntax.md) and [Examples of Database Queries Using SQL and Script](examples-of-database-queries-using-sql-and-script.md).</span></span>

<span data-ttu-id="65f35-107">範例腳本會示範：</span><span class="sxs-lookup"><span data-stu-id="65f35-107">The sample script demonstrates:</span></span>

-   <span data-ttu-id="65f35-108">[**OpenDatabase 方法 (安裝程式物件)**](installer-opendatabase.md)和 [**安裝程式物件**](installer-object.md)的 [**LastErrorRecord 方法**](installer-lasterrorrecord.md)</span><span class="sxs-lookup"><span data-stu-id="65f35-108">[**OpenDatabase method (Installer Object)**](installer-opendatabase.md) and the [**LastErrorRecord method**](installer-lasterrorrecord.md) of the [**Installer Object**](installer-object.md)</span></span>
-   <span data-ttu-id="65f35-109">[**OpenView 方法**](database-openview.md)和 [**Database 物件**](database-object.md)的 [**Commit 方法**](database-commit.md)</span><span class="sxs-lookup"><span data-stu-id="65f35-109">[**OpenView method**](database-openview.md), and the [**Commit method**](database-commit.md) of the [**Database Object**](database-object.md)</span></span>
-   <span data-ttu-id="65f35-110">[](view-execute.md) [ **View 物件** 的 Execute 方法](view-object.md)</span><span class="sxs-lookup"><span data-stu-id="65f35-110">[**Execute method**](view-execute.md) of the [**View Object**](view-object.md)</span></span>
-   <span data-ttu-id="65f35-111">[**至 convertfrom-stringdata 屬性**](record-stringdata.md) Propertyof [**記錄物件**](record-object.md)</span><span class="sxs-lookup"><span data-stu-id="65f35-111">[**StringData property**](record-stringdata.md) propertyof the [**Record Object**](record-object.md)</span></span>

<span data-ttu-id="65f35-112">使用此範例需要 Windows Script Host 的 CScript.exe 或 WScript.exe 版本。</span><span class="sxs-lookup"><span data-stu-id="65f35-112">Using this sample requires the CScript.exe or WScript.exe version of Windows Script Host.</span></span> <span data-ttu-id="65f35-113">若要使用 CScript.exe 執行此範例，請使用下列語法在命令提示字元中輸入命令。</span><span class="sxs-lookup"><span data-stu-id="65f35-113">To use CScript.exe to run this sample, type a command at the command prompt using the following syntax.</span></span> <span data-ttu-id="65f35-114">如果第一個引數是/？，則會顯示說明</span><span class="sxs-lookup"><span data-stu-id="65f35-114">Help is displayed if the first argument is /?</span></span> <span data-ttu-id="65f35-115">或者，如果指定的引數太少。</span><span class="sxs-lookup"><span data-stu-id="65f35-115">or if too few arguments are specified.</span></span> <span data-ttu-id="65f35-116">若要將輸出重新導向至檔案，請以 VBS > 路徑結束命令列 \[  \] 。</span><span class="sxs-lookup"><span data-stu-id="65f35-116">To redirect the output to a file, end the command line with VBS > \[*path to file*\].</span></span> <span data-ttu-id="65f35-117">此範例會傳回值0表示成功，如果叫用說明，則傳回 1; 如果腳本失敗，則傳回2。</span><span class="sxs-lookup"><span data-stu-id="65f35-117">The sample returns a value of 0 for success, 1 if help is invoked, and 2 if the script fails.</span></span>

<span data-ttu-id="65f35-118">**cscript WiRunSQL.vbs \[ 資料庫 \] \[ SQL 查詢的路徑\]**</span><span class="sxs-lookup"><span data-stu-id="65f35-118">**cscript WiRunSQL.vbs \[path to database\]\[SQL queries\]**</span></span>

<span data-ttu-id="65f35-119">指定 Windows Installer 資料庫的路徑。</span><span class="sxs-lookup"><span data-stu-id="65f35-119">Specify the path to a Windows Installer database.</span></span> <span data-ttu-id="65f35-120">指定要執行的 SQL 查詢。</span><span class="sxs-lookup"><span data-stu-id="65f35-120">Specify the SQL queries that are to be executed.</span></span> <span data-ttu-id="65f35-121">請注意，SQL 查詢必須括在雙引號中。</span><span class="sxs-lookup"><span data-stu-id="65f35-121">Note that the SQL query must be enclosed in double quotes.</span></span> <span data-ttu-id="65f35-122">選取 [查詢] 會顯示查詢中所指定之結果清單的資料列。</span><span class="sxs-lookup"><span data-stu-id="65f35-122">SELECT queries display the rows of the result list specified in the query.</span></span> <span data-ttu-id="65f35-123">不會顯示查詢所選取的二進位資料行。</span><span class="sxs-lookup"><span data-stu-id="65f35-123">Binary data columns selected by a query are not displayed.</span></span>

<span data-ttu-id="65f35-124">如需其他腳本範例，請參閱 [Windows Installer 腳本範例](windows-installer-scripting-examples.md)。</span><span class="sxs-lookup"><span data-stu-id="65f35-124">For additional scripting examples, see [Windows Installer Scripting Examples](windows-installer-scripting-examples.md).</span></span> <span data-ttu-id="65f35-125">如需不需要 Windows Script Host 的範例公用程式，請參閱 [Windows Installer 開發工具](windows-installer-development-tools.md)。</span><span class="sxs-lookup"><span data-stu-id="65f35-125">For sample utilities that do not require Windows Script Host, see [Windows Installer Development Tools](windows-installer-development-tools.md).</span></span>

<span data-ttu-id="65f35-126">如需詳細資訊，請參閱[使用 SQL 和腳本](examples-of-database-queries-using-sql-and-script.md)[處理查詢](working-with-queries.md)和資料庫查詢範例。</span><span class="sxs-lookup"><span data-stu-id="65f35-126">For more information, see [Working with Queries](working-with-queries.md) and [Examples of Database Queries Using SQL and Script](examples-of-database-queries-using-sql-and-script.md).</span></span> <span data-ttu-id="65f35-127">範例 [當地語系化範例](a-localization-example.md) 示範如何使用 SQL 來 [當地語系化資料庫資料行](localizing-database-columns.md) ，以及 [更新摘要資訊資料流程](updating-a-summary-information-stream.md)。</span><span class="sxs-lookup"><span data-stu-id="65f35-127">The sample [A Localization Example](a-localization-example.md) demonstrates using SQL for [Localizing Database Columns](localizing-database-columns.md) and [Updating a Summary Information Stream](updating-a-summary-information-stream.md).</span></span>

 

 



