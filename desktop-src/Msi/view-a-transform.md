---
description: Windows Installer 開發人員 Windows SDK 元件中提供了 VBScript 檔案 WiLstXfm.vbs。 這個腳本範例可以用來查看轉換檔。
ms.assetid: c2e3dd56-b0e5-481a-b7b8-5000fa686850
title: 查看轉換
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 69f4a858f8deb115de967da3b4d485b596f85cee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106971196"
---
# <a name="view-a-transform"></a><span data-ttu-id="019ff-104">查看轉換</span><span class="sxs-lookup"><span data-stu-id="019ff-104">View a Transform</span></span>

<span data-ttu-id="019ff-105">[Windows Installer 開發人員 Windows SDK 元件](platform-sdk-components-for-windows-installer-developers.md)中提供了 VBScript 檔案 WiLstXfm.vbs。</span><span class="sxs-lookup"><span data-stu-id="019ff-105">The VBScript file WiLstXfm.vbs is provided in the [Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).</span></span> <span data-ttu-id="019ff-106">這個腳本範例可以用來查看轉換檔。</span><span class="sxs-lookup"><span data-stu-id="019ff-106">This script sample can be used to view a transform file.</span></span>

<span data-ttu-id="019ff-107">此範例將示範如何使用：</span><span class="sxs-lookup"><span data-stu-id="019ff-107">The sample demonstrates the use of:</span></span>

-   [<span data-ttu-id="019ff-108">\_TransformView 資料表</span><span class="sxs-lookup"><span data-stu-id="019ff-108">\_TransformView table</span></span>](-transformview-table.md)
-   [<span data-ttu-id="019ff-109">**(安裝程式物件) 的 OpenDatabase 方法**</span><span class="sxs-lookup"><span data-stu-id="019ff-109">**OpenDatabase method (Installer Object)**</span></span>](installer-opendatabase.md)
-   <span data-ttu-id="019ff-110">[](installer-lasterrorrecord.md) [**安裝程式物件** 的 LastErrorRecord 方法](installer-object.md)</span><span class="sxs-lookup"><span data-stu-id="019ff-110">[**LastErrorRecord method**](installer-lasterrorrecord.md) of the [**Installer object**](installer-object.md)</span></span>
-   [<span data-ttu-id="019ff-111">**ApplyTransform 方法**</span><span class="sxs-lookup"><span data-stu-id="019ff-111">**ApplyTransform method**</span></span>](database-applytransform.md)
-   [<span data-ttu-id="019ff-112">**OpenView 方法**</span><span class="sxs-lookup"><span data-stu-id="019ff-112">**OpenView method**</span></span>](database-openview.md)
-   <span data-ttu-id="019ff-113">[](database-commit.md) [ **Database 物件** 的 Commit 方法](database-object.md)</span><span class="sxs-lookup"><span data-stu-id="019ff-113">[**Commit method**](database-commit.md) of the [**Database object**](database-object.md)</span></span>
-   [<span data-ttu-id="019ff-114">**IsNull 屬性**</span><span class="sxs-lookup"><span data-stu-id="019ff-114">**IsNull property**</span></span>](record-isnull.md)
-   <span data-ttu-id="019ff-115">[](record-stringdata.md) [ **Record 物件** 的至 convertfrom-stringdata 屬性](record-object.md)</span><span class="sxs-lookup"><span data-stu-id="019ff-115">[**StringData property**](record-stringdata.md) of the [**Record object**](record-object.md)</span></span>

<span data-ttu-id="019ff-116">使用此範例需要 CScript.exe 版本的 Windows Script Host。</span><span class="sxs-lookup"><span data-stu-id="019ff-116">Using this sample requires the CScript.exe version of Windows Script Host.</span></span> <span data-ttu-id="019ff-117">若要使用 CScript.exe 執行此範例，請使用下列語法在命令提示字元中輸入命令。</span><span class="sxs-lookup"><span data-stu-id="019ff-117">To use CScript.exe to run this sample, type a command at the command prompt using the following syntax.</span></span> <span data-ttu-id="019ff-118">如果第一個引數是/？，則會顯示說明</span><span class="sxs-lookup"><span data-stu-id="019ff-118">Help is displayed if the first argument is /?</span></span> <span data-ttu-id="019ff-119">或者，如果指定的引數太少。</span><span class="sxs-lookup"><span data-stu-id="019ff-119">or if too few arguments are specified.</span></span> <span data-ttu-id="019ff-120">若要將輸出重新導向至檔案，請以 VBS > 路徑結束命令列 \[  \] 。</span><span class="sxs-lookup"><span data-stu-id="019ff-120">To redirect the output to a file, end the command line with VBS > \[*path to file*\].</span></span> <span data-ttu-id="019ff-121">此範例會傳回值0表示成功，如果叫用說明，則傳回 1; 如果腳本失敗，則傳回2。</span><span class="sxs-lookup"><span data-stu-id="019ff-121">The sample returns a value of 0 for success, 1 if help is invoked, and 2 if the script fails.</span></span>

<span data-ttu-id="019ff-122">**cscript WiLstXfm.vbs** *\[ 路徑參考要 \] \[ \] \[ 查看 \] 的轉換資料庫選項路徑*</span><span class="sxs-lookup"><span data-stu-id="019ff-122">**cscript WiLstXfm.vbs** *\[path to reference database\]\[option\]\[path to transform to be viewed\]*</span></span>

<span data-ttu-id="019ff-123">指定參考 Windows Installer 資料庫的路徑。</span><span class="sxs-lookup"><span data-stu-id="019ff-123">Specify the path to the reference Windows Installer database.</span></span> <span data-ttu-id="019ff-124">指定要用來轉換所要查看之檔案的路徑清單。</span><span class="sxs-lookup"><span data-stu-id="019ff-124">Specify a list of paths to transform files that are being viewed.</span></span> <span data-ttu-id="019ff-125">清單中的每個路徑前面都有一個選擇性數值。</span><span class="sxs-lookup"><span data-stu-id="019ff-125">Each path in the list may by preceded by an optional numeric value.</span></span> <span data-ttu-id="019ff-126">此值會指定要隱藏的一組錯誤條件。</span><span class="sxs-lookup"><span data-stu-id="019ff-126">This value specifies a set of error conditions that are to be suppressed.</span></span> <span data-ttu-id="019ff-127">您可以將這些值加在一起，以隱藏多個條件。</span><span class="sxs-lookup"><span data-stu-id="019ff-127">You may add these values together to suppress multiple conditions.</span></span> <span data-ttu-id="019ff-128">如果未指定數值選項，則會隱藏所有錯誤條件。</span><span class="sxs-lookup"><span data-stu-id="019ff-128">If no numeric option is specified, all the error conditions are suppressed.</span></span> <span data-ttu-id="019ff-129">這份清單中的引數會以從左至右的循序執行，在命令列上顯示這些引數。</span><span class="sxs-lookup"><span data-stu-id="019ff-129">The arguments in this list are executed in the left-to-right order in which they appear on the command line.</span></span>



| <span data-ttu-id="019ff-130">值</span><span class="sxs-lookup"><span data-stu-id="019ff-130">Value</span></span> | <span data-ttu-id="019ff-131">要隱藏的錯誤條件</span><span class="sxs-lookup"><span data-stu-id="019ff-131">Error condition to suppress</span></span>                   |
|-------|-----------------------------------------------|
| <span data-ttu-id="019ff-132">1</span><span class="sxs-lookup"><span data-stu-id="019ff-132">1</span></span>     | <span data-ttu-id="019ff-133">加入已經存在的資料列。</span><span class="sxs-lookup"><span data-stu-id="019ff-133">Adding a row that already exists.</span></span>             |
| <span data-ttu-id="019ff-134">2</span><span class="sxs-lookup"><span data-stu-id="019ff-134">2</span></span>     | <span data-ttu-id="019ff-135">正在刪除不存在的資料列。</span><span class="sxs-lookup"><span data-stu-id="019ff-135">Deleting a row that does not exist.</span></span>           |
| <span data-ttu-id="019ff-136">4</span><span class="sxs-lookup"><span data-stu-id="019ff-136">4</span></span>     | <span data-ttu-id="019ff-137">加入已經存在的資料表。</span><span class="sxs-lookup"><span data-stu-id="019ff-137">Adding a table that already exists.</span></span>           |
| <span data-ttu-id="019ff-138">8</span><span class="sxs-lookup"><span data-stu-id="019ff-138">8</span></span>     | <span data-ttu-id="019ff-139">正在刪除不存在的資料表。</span><span class="sxs-lookup"><span data-stu-id="019ff-139">Deleting a table that does not exist.</span></span>         |
| <span data-ttu-id="019ff-140">16</span><span class="sxs-lookup"><span data-stu-id="019ff-140">16</span></span>    | <span data-ttu-id="019ff-141">正在更新不存在的資料列。</span><span class="sxs-lookup"><span data-stu-id="019ff-141">Updating a row that does not exist.</span></span>           |
| <span data-ttu-id="019ff-142">256</span><span class="sxs-lookup"><span data-stu-id="019ff-142">256</span></span>   | <span data-ttu-id="019ff-143">資料庫與轉換字碼頁不相符。</span><span class="sxs-lookup"><span data-stu-id="019ff-143">Mismatch of database and transform codepages.</span></span> |



 

<span data-ttu-id="019ff-144">如需其他腳本範例，請參閱 [Windows Installer 腳本範例](windows-installer-scripting-examples.md)。</span><span class="sxs-lookup"><span data-stu-id="019ff-144">For additional scripting examples, see [Windows Installer Scripting Examples](windows-installer-scripting-examples.md).</span></span> <span data-ttu-id="019ff-145">如需不需要 Windows Script Host 的範例公用程式，請參閱 [Windows Installer 開發工具](windows-installer-development-tools.md)。</span><span class="sxs-lookup"><span data-stu-id="019ff-145">For sample utilities that do not require Windows Script Host, see [Windows Installer Development Tools](windows-installer-development-tools.md).</span></span>

 

 



