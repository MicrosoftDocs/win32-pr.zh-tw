---
description: Windows Installer 開發人員 Windows SDK 元件中提供了 VBScript 檔案 WiUseXfm.vbs。 這個範例會示範如何使用腳本將轉換套用至 Windows Installer 資料庫。
ms.assetid: e647388e-5211-463d-9e3e-b502af01fc0c
title: 套用轉換
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9e86acc495fc2a0bb8dff562832e58d29483256
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848975"
---
# <a name="apply-a-transform"></a><span data-ttu-id="5cc3e-104">套用轉換</span><span class="sxs-lookup"><span data-stu-id="5cc3e-104">Apply a Transform</span></span>

<span data-ttu-id="5cc3e-105">[Windows Installer 開發人員 Windows SDK 元件](platform-sdk-components-for-windows-installer-developers.md)中提供了 VBScript 檔案 WiUseXfm.vbs。</span><span class="sxs-lookup"><span data-stu-id="5cc3e-105">The VBScript file WiUseXfm.vbs is provided in the [Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).</span></span> <span data-ttu-id="5cc3e-106">這個範例會示範如何使用腳本將轉換套用至 Windows Installer 資料庫。</span><span class="sxs-lookup"><span data-stu-id="5cc3e-106">This sample shows how script can be used to apply a transform to a Windows Installer database.</span></span>

<span data-ttu-id="5cc3e-107">此範例示範如何使用</span><span class="sxs-lookup"><span data-stu-id="5cc3e-107">The sample demonstrates the use of</span></span>

-   [<span data-ttu-id="5cc3e-108">**(安裝程式物件) 的 OpenDatabase 方法**</span><span class="sxs-lookup"><span data-stu-id="5cc3e-108">**OpenDatabase method (Installer Object)**</span></span>](installer-opendatabase.md)
-   <span data-ttu-id="5cc3e-109">[](installer-lasterrorrecord.md) [**安裝程式物件** 的 LastErrorRecord 方法](installer-object.md)</span><span class="sxs-lookup"><span data-stu-id="5cc3e-109">[**LastErrorRecord method**](installer-lasterrorrecord.md) of the [**Installer object**](installer-object.md)</span></span>
-   [<span data-ttu-id="5cc3e-110">**ApplyTransform 方法**</span><span class="sxs-lookup"><span data-stu-id="5cc3e-110">**ApplyTransform method**</span></span>](database-applytransform.md)
-   <span data-ttu-id="5cc3e-111">[](database-commit.md) [ **Database 物件** 的 Commit 方法](database-object.md)</span><span class="sxs-lookup"><span data-stu-id="5cc3e-111">[**Commit method**](database-commit.md) of the [**Database object**](database-object.md)</span></span>

<span data-ttu-id="5cc3e-112">您將需要 CScript.exe 或 WScript.exe 版本的 Windows Script Host 才能使用此範例。</span><span class="sxs-lookup"><span data-stu-id="5cc3e-112">You'll require the CScript.exe or WScript.exe version of Windows Script Host to use this sample.</span></span> <span data-ttu-id="5cc3e-113">若要使用 CScript.exe 執行此範例，請使用下列語法在命令提示字元中輸入命令列。</span><span class="sxs-lookup"><span data-stu-id="5cc3e-113">To use CScript.exe to run this sample, type a command line at the command prompt using the following syntax.</span></span> <span data-ttu-id="5cc3e-114">如果第一個引數是/？，則會顯示說明</span><span class="sxs-lookup"><span data-stu-id="5cc3e-114">Help is displayed if the first argument is /?</span></span> <span data-ttu-id="5cc3e-115">或者，如果指定的引數太少。</span><span class="sxs-lookup"><span data-stu-id="5cc3e-115">or if too few arguments are specified.</span></span> <span data-ttu-id="5cc3e-116">若要將輸出重新導向至檔案，請以 VBS > 路徑結束命令列 \[  \] 。</span><span class="sxs-lookup"><span data-stu-id="5cc3e-116">To redirect the output to a file, end the command line with VBS > \[*path to file*\].</span></span> <span data-ttu-id="5cc3e-117">此範例會傳回值0表示成功，如果叫用說明，則傳回 1; 如果腳本失敗，則傳回2。</span><span class="sxs-lookup"><span data-stu-id="5cc3e-117">The sample returns a value of 0 for success, 1 if help is invoked, and 2 if the script fails.</span></span>

<span data-ttu-id="5cc3e-118">**轉換檔案 \[ 選項之原始資料庫 \] \[ 路徑的 \] cscript WiUseXfm.vbs 路徑 \[\]**</span><span class="sxs-lookup"><span data-stu-id="5cc3e-118">**cscript WiUseXfm.vbs \[path to original database\]\[path to transform file\]\[options\]**</span></span>

<span data-ttu-id="5cc3e-119">指定 Windows Installer 資料庫的路徑。</span><span class="sxs-lookup"><span data-stu-id="5cc3e-119">Specify the path to the Windows Installer database.</span></span> <span data-ttu-id="5cc3e-120">指定轉換檔案的路徑。</span><span class="sxs-lookup"><span data-stu-id="5cc3e-120">Specify the path to the transform file.</span></span> <span data-ttu-id="5cc3e-121">如果省略轉換檔的路徑，則只會比較兩個資料庫。</span><span class="sxs-lookup"><span data-stu-id="5cc3e-121">If the path to the transform file is omitted, the two databases are only compared.</span></span> <span data-ttu-id="5cc3e-122">第三個引數是選擇性的數值，指定要隱藏的一組錯誤條件。</span><span class="sxs-lookup"><span data-stu-id="5cc3e-122">The third argument is an optional numeric value that specifies a set of error conditions that are to be suppressed.</span></span> <span data-ttu-id="5cc3e-123">將這些值加在一起，以隱藏多個條件。</span><span class="sxs-lookup"><span data-stu-id="5cc3e-123">Add these values together to suppress multiple conditions.</span></span>



| <span data-ttu-id="5cc3e-124">值</span><span class="sxs-lookup"><span data-stu-id="5cc3e-124">Value</span></span> | <span data-ttu-id="5cc3e-125">要隱藏的錯誤條件</span><span class="sxs-lookup"><span data-stu-id="5cc3e-125">Error condition to suppress</span></span>                   |
|-------|-----------------------------------------------|
| <span data-ttu-id="5cc3e-126">1</span><span class="sxs-lookup"><span data-stu-id="5cc3e-126">1</span></span>     | <span data-ttu-id="5cc3e-127">加入已經存在的資料列。</span><span class="sxs-lookup"><span data-stu-id="5cc3e-127">Adding a row that already exists.</span></span>             |
| <span data-ttu-id="5cc3e-128">2</span><span class="sxs-lookup"><span data-stu-id="5cc3e-128">2</span></span>     | <span data-ttu-id="5cc3e-129">正在刪除不存在的資料列。</span><span class="sxs-lookup"><span data-stu-id="5cc3e-129">Deleting a row that does not exist.</span></span>           |
| <span data-ttu-id="5cc3e-130">4</span><span class="sxs-lookup"><span data-stu-id="5cc3e-130">4</span></span>     | <span data-ttu-id="5cc3e-131">加入已經存在的資料表。</span><span class="sxs-lookup"><span data-stu-id="5cc3e-131">Adding a table that already exists.</span></span>           |
| <span data-ttu-id="5cc3e-132">8</span><span class="sxs-lookup"><span data-stu-id="5cc3e-132">8</span></span>     | <span data-ttu-id="5cc3e-133">正在刪除不存在的資料表。</span><span class="sxs-lookup"><span data-stu-id="5cc3e-133">Deleting a table that does not exist.</span></span>         |
| <span data-ttu-id="5cc3e-134">16</span><span class="sxs-lookup"><span data-stu-id="5cc3e-134">16</span></span>    | <span data-ttu-id="5cc3e-135">正在更新不存在的資料列。</span><span class="sxs-lookup"><span data-stu-id="5cc3e-135">Updating a row that does not exist.</span></span>           |
| <span data-ttu-id="5cc3e-136">256</span><span class="sxs-lookup"><span data-stu-id="5cc3e-136">256</span></span>   | <span data-ttu-id="5cc3e-137">資料庫與轉換字碼頁不相符。</span><span class="sxs-lookup"><span data-stu-id="5cc3e-137">Mismatch of database and transform codepages.</span></span> |



 

<span data-ttu-id="5cc3e-138">如需其他腳本範例，請參閱 [Windows Installer 腳本範例](windows-installer-scripting-examples.md)。</span><span class="sxs-lookup"><span data-stu-id="5cc3e-138">For additional scripting examples, see [Windows Installer Scripting Examples](windows-installer-scripting-examples.md).</span></span> <span data-ttu-id="5cc3e-139">如需不需要 Windows Script Host 的範例公用程式，請參閱 [Windows Installer 開發工具](windows-installer-development-tools.md)。</span><span class="sxs-lookup"><span data-stu-id="5cc3e-139">For sample utilities that do not require Windows Script Host, see [Windows Installer Development Tools](windows-installer-development-tools.md).</span></span>

 

 



